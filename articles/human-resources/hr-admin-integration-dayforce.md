---
title: تكوين التكامل مع Dayforce
description: يعتمد التكامل بين Microsoft Dynamics 365 Human Resources وCeridian Dayforce على العديد من خطوات التكوين الموضحة في هذا المقال. يجب عليك تكوين التكامل في كل من Human Resources وDayforce قبل أن تتمكن من معالجة دورة دفع.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051487"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="b5534-104">تكوين التكامل مع Dayforce </span><span class="sxs-lookup"><span data-stu-id="b5534-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b5534-105">يعتمد التكامل بين Microsoft Dynamics 365 Human Resources وCeridian Dayforce على العديد من خطوات التكوين الموضحة في هذا المقال.</span><span class="sxs-lookup"><span data-stu-id="b5534-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="b5534-106">يجب عليك تكوين التكامل في كل من Human Resources وDayforce قبل أن تتمكن من معالجة دورة دفع.</span><span class="sxs-lookup"><span data-stu-id="b5534-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b5534-107">عندما تستخدم خدمة مثل Dayforce لإتمام دورات الدفع، يجب عليك تمكين التكامل في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b5534-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="b5534-108">يتطلب التكامل بيانات معينة من Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b5534-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="b5534-109">لذلك، يجب عليك التأكد من أن البيانات التي تم تعيينها إلى Dayforce هي بيانات تم تكوينها في Human Resources بطريقة تدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="b5534-110">يستخدم التكامل الفئات الواسعة التالية من البيانات:</span><span class="sxs-lookup"><span data-stu-id="b5534-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b5534-111">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-111">Human resources data</span></span>
- <span data-ttu-id="b5534-112">بيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-112">Compensation data</span></span>
- <span data-ttu-id="b5534-113">بيانات كشف المرتبات، مثل دورات الدفع وفترات الدفع وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b5534-114">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-114">Worker data</span></span>

<span data-ttu-id="b5534-115">يصف هذا المقال الخطوات التي يجب اتباعها لتمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b5534-116">ويشرح أيضًا أنواع البيانات وتفاصيل التكوين التي يحتاج إليها التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b5534-117">تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="b5534-117">Enable the integration</span></span>

<span data-ttu-id="b5534-118">في Human Resources، يجب تشغيل التكامل وإدخال معلومات التكوين للاتصال بخدمة Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b5534-119">إذا أردت أن يتم استيراد حركة دفتر الأستاذ العام التي نشأت إلى Microsoft Dynamics 365 Finance، فيجب أيضًا إعداد حساب تخزين في Microsoft Azure وإدخال سلسلة اتصال Azure Storage في Finance.</span><span class="sxs-lookup"><span data-stu-id="b5534-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="b5534-120">لتشغيل التكامل في Human Resources، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b5534-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="b5534-121">في صفحة **إدارة النظام**، حدد **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="b5534-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b5534-122">أدخل نقطة نهاية بروتوكول نقل الملفات (FTP) الآمنة ومسار مجلد FTP الآمن.</span><span class="sxs-lookup"><span data-stu-id="b5534-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b5534-123">أدخل اسم المستخدم وكلمة المرور للمستخدم الذي سينتقل إلى نقطة النهاية الآمنة ومسار المجلد الآمن في بروتوكول FTP.</span><span class="sxs-lookup"><span data-stu-id="b5534-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b5534-124">اختبر الاتصال، كما تقتضي الحاجة، وعيّن الخيار **تمكين تكامل كشف المرتبات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b5534-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b5534-125">عند تشغيل التكامل، يتم إنشاء حزمة وملفات تصدير البيانات ويتم تعيين معدل التكرار.</span><span class="sxs-lookup"><span data-stu-id="b5534-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b5534-126">ويمكنك تغيير معدل التكرار وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="b5534-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="b5534-127">لمزيد من المعلومات حول حسابات مساحة تخزين Azure وسلاسل اتصال مساحة تخزين Azure، راجع مقالات Azure التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="b5534-128">حول حسابات مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="b5534-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b5534-129">تكوين سلاسل اتصال مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="b5534-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="b5534-130">تفاصيل تقنية عند تمكين تكامل الرواتب</span><span class="sxs-lookup"><span data-stu-id="b5534-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="b5534-131">يؤدي تشغيل تكامل الرواتب إلى تأثيرين أساسيين:</span><span class="sxs-lookup"><span data-stu-id="b5534-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="b5534-132">يتم إنشاء مشروع تصدير بيانات يُسمى "تصدير تكامل الرواتب".</span><span class="sxs-lookup"><span data-stu-id="b5534-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="b5534-133">يحتوي هذا المشروع على الكيانات والحقول المطلوبة لتكامل الرواتب.</span><span class="sxs-lookup"><span data-stu-id="b5534-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="b5534-134">لفحص المشروع، انتقل إلى **إدارة النظام**، وحدد تجانب **إدارة البيانات**، ثم افتح مشروع البيانات من قائمة المشروعات.</span><span class="sxs-lookup"><span data-stu-id="b5534-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="b5534-135">تنفذ هذه الوظيفة الدفعية مشروع تصدير البيانات، وتشفر حزمة البيانات الناتجة، وتنقل ملف حزمة البيانات إلى نقطة نهاية SFTP التي تم تكوينها على شاشة **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="b5534-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="b5534-136">يتم تشفير حزمة البيانات التي تم نقلها إلى نقطة نهاية SFTP باستخدام مفتاح فريد للحزمة.</span><span class="sxs-lookup"><span data-stu-id="b5534-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="b5534-137">المفتاح موجود في Azure Key Vault والذي يمكن الوصول إليه عن طريق Ceridian فقط.</span><span class="sxs-lookup"><span data-stu-id="b5534-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="b5534-138">لا يمكن فك تشفير محتويات حزمة البيانات وفحصها.</span><span class="sxs-lookup"><span data-stu-id="b5534-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="b5534-139">إذا كنت بحاجة إلى فحص محتويات حزمة البيانات، ستحتاج إلى تصدير مشروع البيانات "تصدير تكامل الرواتب" يدويا، وتنزيله، ثم فتحه.</span><span class="sxs-lookup"><span data-stu-id="b5534-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="b5534-140">لن تطبق عملية التصدير اليدوية التشفير أو نقل الحزمة.</span><span class="sxs-lookup"><span data-stu-id="b5534-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="b5534-141">بالنسبة للمثيلات التي يتم فيها إرسال ملفات التكامل من Dynamics 365 Human Resources UAT أو بيئة اختبار معزولة إلى بيئة Ceridian Dayforce Test، يمكنك استخدام عنوان URL للمخزن الرئيسي التالي: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="b5534-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="b5534-142">تكوين بياناتك</span><span class="sxs-lookup"><span data-stu-id="b5534-142">Configure your data</span></span> 

<span data-ttu-id="b5534-143">لمعالجة كشف، يجب عليك تكوين بيانات Human Resources في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b5534-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="b5534-144">يجب إعداد بيانات المؤسسة، مثل الوظائف والمناصب، مع معلومات الميزات والتعويضات.</span><span class="sxs-lookup"><span data-stu-id="b5534-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b5534-145">تتعلق هذه المعلومات بالتوظيف والدفع والخصم وهي معلومات مطلوبة لإنشاء عملية الدفع للموظفين.</span><span class="sxs-lookup"><span data-stu-id="b5534-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b5534-146">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b5534-147">ميزات</span><span class="sxs-lookup"><span data-stu-id="b5534-147">Benefits</span></span> 

<span data-ttu-id="b5534-148">توفر الموارد البشرية أدوات يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العاملين التي تقدمها مؤسسة أو تعالجها للعاملين فيها.</span><span class="sxs-lookup"><span data-stu-id="b5534-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b5534-149">عندما إنشاء ميزات، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b5534-150">خطط الميزات</span><span class="sxs-lookup"><span data-stu-id="b5534-150">Benefit plans</span></span>

- <span data-ttu-id="b5534-151">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-151">Plan (required)</span></span>
- <span data-ttu-id="b5534-152">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-152">Type (required)</span></span>
- <span data-ttu-id="b5534-153">تأثير كشف المرتبات (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-153">Payroll impact (required)</span></span>
- <span data-ttu-id="b5534-154">استرداد المتأخرات</span><span class="sxs-lookup"><span data-stu-id="b5534-154">Recover arrears</span></span>
- <span data-ttu-id="b5534-155">أسلوب الخصم</span><span class="sxs-lookup"><span data-stu-id="b5534-155">Deduction method</span></span>
- <span data-ttu-id="b5534-156">أولوية الخصم</span><span class="sxs-lookup"><span data-stu-id="b5534-156">Deduction priority</span></span>
- <span data-ttu-id="b5534-157">حد الفترة</span><span class="sxs-lookup"><span data-stu-id="b5534-157">Limit period</span></span>
- <span data-ttu-id="b5534-158">تحديد المبلغ</span><span class="sxs-lookup"><span data-stu-id="b5534-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b5534-159">ميزات</span><span class="sxs-lookup"><span data-stu-id="b5534-159">Benefits</span></span>

- <span data-ttu-id="b5534-160">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-160">Plan (required)</span></span>
- <span data-ttu-id="b5534-161">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-161">Type (required)</span></span>
- <span data-ttu-id="b5534-162">الخيار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-162">Option (required)</span></span>
- <span data-ttu-id="b5534-163">معرّف الميزة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-163">Benefit ID (required)</span></span>
- <span data-ttu-id="b5534-164">التكرار</span><span class="sxs-lookup"><span data-stu-id="b5534-164">Frequency</span></span>
- <span data-ttu-id="b5534-165">أساس</span><span class="sxs-lookup"><span data-stu-id="b5534-165">Basis</span></span>
- <span data-ttu-id="b5534-166">المبلغ أو النسبة</span><span class="sxs-lookup"><span data-stu-id="b5534-166">Amount or rate</span></span>
- <span data-ttu-id="b5534-167">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b5534-168">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b5534-168">Supported frequencies</span></span> 

- <span data-ttu-id="b5534-169">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="b5534-169">Weekly</span></span>
- <span data-ttu-id="b5534-170">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="b5534-170">Bi-weekly</span></span>
- <span data-ttu-id="b5534-171">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="b5534-171">Semi-monthly</span></span>
- <span data-ttu-id="b5534-172">شهري</span><span class="sxs-lookup"><span data-stu-id="b5534-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b5534-173">الأسس المدعومة</span><span class="sxs-lookup"><span data-stu-id="b5534-173">Supported bases</span></span> 

- <span data-ttu-id="b5534-174">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="b5534-174">Fixed amount</span></span>
- <span data-ttu-id="b5534-175">النسبة المئوية للأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-175">Percent of earnings</span></span>
- <span data-ttu-id="b5534-176">ساعات الإنتاج</span><span class="sxs-lookup"><span data-stu-id="b5534-176">Productive hours</span></span>

<span data-ttu-id="b5534-177">تنشئ خدمة Dayforce الخصومات التالية، استنادًا إلى تأثير كشف المرتبات المحدد في خطة الميزات.</span><span class="sxs-lookup"><span data-stu-id="b5534-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b5534-178">التحديد في Human Resources</span><span class="sxs-lookup"><span data-stu-id="b5534-178">Selection in Human Resources</span></span>        | <span data-ttu-id="b5534-179">النتيجة في Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b5534-180">لا‬‬ شيء</span><span class="sxs-lookup"><span data-stu-id="b5534-180">None</span></span>                       | <span data-ttu-id="b5534-181">لا يتم إنشاء أي خصم.</span><span class="sxs-lookup"><span data-stu-id="b5534-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="b5534-182">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="b5534-182">Deduction only</span></span>             | <span data-ttu-id="b5534-183">يتم إنشاء خصم الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b5534-184">المساهمة فقط</span><span class="sxs-lookup"><span data-stu-id="b5534-184">Contribution only</span></span>          | <span data-ttu-id="b5534-185">يتم إنشاء خصم صاحب العمل‬.</span><span class="sxs-lookup"><span data-stu-id="b5534-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b5534-186">الخصم والمساهمة</span><span class="sxs-lookup"><span data-stu-id="b5534-186">Deduction and contribution</span></span> | <span data-ttu-id="b5534-187">يتم إنشاء خصومات الموظف وصاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="b5534-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b5534-188">لمزيد من المعلومات حول كيفية تحديد وإدارة برنامج ميزات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="b5534-189">تقديم برنامج ميزات الموظفين</span><span class="sxs-lookup"><span data-stu-id="b5534-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b5534-190">إنشاء ميزة جديدة</span><span class="sxs-lookup"><span data-stu-id="b5534-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b5534-191">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="b5534-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b5534-192">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="b5534-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b5534-193">التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-193">Compensation</span></span> 

<span data-ttu-id="b5534-194">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="b5534-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b5534-195">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="b5534-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b5534-196">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="b5534-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b5534-197">تستخدم خدمة Dayforce معلومات التعويض لحساب معدل الموظف السنوي أو الساعي.</span><span class="sxs-lookup"><span data-stu-id="b5534-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b5534-198">وتعتبر خطط التعويض الثابت وتحويلات معدل الدفع مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b5534-199">يجب ربط الموظفين بخطة تعويض ثابت.</span><span class="sxs-lookup"><span data-stu-id="b5534-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b5534-200">لمزيد من المعلومات حول خطط التعويض، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="b5534-201">إنشاء خطط التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="b5534-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b5534-202">إنشاء خطط التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="b5534-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b5534-203">تطوير خطط وبنية المرتب/التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b5534-204">تعويض العملية</span><span class="sxs-lookup"><span data-stu-id="b5534-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b5534-205">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="b5534-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b5534-206">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="b5534-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b5534-207">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="b5534-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b5534-208">الوظائف</span><span class="sxs-lookup"><span data-stu-id="b5534-208">Jobs</span></span> 

<span data-ttu-id="b5534-209">الوظيفة هي مجموعة من المهام والمسؤوليات المطلوبة من الشخص الذي يؤدي وظيفة.</span><span class="sxs-lookup"><span data-stu-id="b5534-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b5534-210">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b5534-211">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="b5534-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b5534-212">تحديد الوظائف الجديدة</span><span class="sxs-lookup"><span data-stu-id="b5534-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b5534-213">المناصب‬</span><span class="sxs-lookup"><span data-stu-id="b5534-213">Positions</span></span>

<span data-ttu-id="b5534-214">يعتبر المنصب مثيلاً فرديًا لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="b5534-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="b5534-215">على سبيل المثال، المنصب "مدير المبيعات (شرق)،" هو أحد المناصب المقترنة بالوظيفة، "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="b5534-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b5534-216">يوجد منصب في قسم.</span><span class="sxs-lookup"><span data-stu-id="b5534-216">A position exists in a department.</span></span> <span data-ttu-id="b5534-217">ويمكن ربط عامل واحد فقط بكل منصب.</span><span class="sxs-lookup"><span data-stu-id="b5534-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b5534-218">عند إعداد المناصب، يجب أخذ البيانات والتكوينات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="b5534-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b5534-219">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-219">Position (required)</span></span>
- <span data-ttu-id="b5534-220">الوصف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-220">Description (required)</span></span>
- <span data-ttu-id="b5534-221">الوظيف (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-221">Job (required)</span></span>
- <span data-ttu-id="b5534-222">القسم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-222">Department (required)</span></span>
- <span data-ttu-id="b5534-223">نوع المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-223">Position type (required)</span></span>
- <span data-ttu-id="b5534-224">مكافئ الوقت الكامل</span><span class="sxs-lookup"><span data-stu-id="b5534-224">Full-time equivalent</span></span>
- <span data-ttu-id="b5534-225">الساعات العادية السنوية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="b5534-226">الدفع بواسطة الكيان القانوني (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b5534-227">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-227">Pay cycle (required)</span></span>
- <span data-ttu-id="b5534-228">البعد المالي الافتراضي – مركز التكلفة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b5534-229">تعيين العامل – العامل وبدء التعيين وانتهاء التعيين وكود السبب</span><span class="sxs-lookup"><span data-stu-id="b5534-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b5534-230">عند ارتباط مناصب متعددة في القسم نفسه بالوظيفة نفسها، فسيتم دمجها في منصب واحد في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b5534-231">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b5534-232">تنظيم القوى العاملة باستخدام الإدارات والوظائف والمناصب</span><span class="sxs-lookup"><span data-stu-id="b5534-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b5534-233">إعداد المناصب</span><span class="sxs-lookup"><span data-stu-id="b5534-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b5534-234">الأقسام</span><span class="sxs-lookup"><span data-stu-id="b5534-234">Departments</span></span>

<span data-ttu-id="b5534-235">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="b5534-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b5534-236">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="b5534-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b5534-237">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="b5534-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b5534-238">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="b5534-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b5534-239">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b5534-240">إنشاء قسم وإقرانه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="b5534-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b5534-241">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="b5534-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b5534-242">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="b5534-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="b5534-243">تحدد دورة الدفع معدل تكرار دفع المرتبات والأيام المحددة التي تُدفع فيها الأجور للعاملين.</span><span class="sxs-lookup"><span data-stu-id="b5534-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b5534-244">على سبيل المثال، قد تكون دورة الدفع الشهرية وقد تُدفع الأجور للعاملين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="b5534-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b5534-245">أو، قد تكون دورة الدفع أسبوعية وقد يحصل الموظفون على رواتبهم يوم الثلاثاء بعد انتهاء فترة الدفع.</span><span class="sxs-lookup"><span data-stu-id="b5534-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b5534-246">يتم تعيين دورات الدفع إلى مناصب للتحكم في الوقت الذي يتم فيه دفع أجور العاملين في هذه المناصب.</span><span class="sxs-lookup"><span data-stu-id="b5534-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b5534-247">بعد إنشاء دورات الدفع، يمكنك إنشاء فترات دفع لكل دورة.</span><span class="sxs-lookup"><span data-stu-id="b5534-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b5534-248">تتضمن كل فترة دفع تاريخ دفع افتراضيًا يستند إلى المعلومات التي توفرها.</span><span class="sxs-lookup"><span data-stu-id="b5534-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b5534-249">ومع ذلك، يمكنك تعديل تاريخ الدفع الافتراضي في فترة دفع للسماح بالاستثناءات، مثل عندما يقع تاريخ الدفع يوم عطلة.</span><span class="sxs-lookup"><span data-stu-id="b5534-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b5534-250">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b5534-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b5534-251">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-251">Pay cycle (required)</span></span>
- <span data-ttu-id="b5534-252">تكرار دورة الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b5534-253">تاريخ بدء الفترة (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b5534-254">تاريخ الدفع الافتراضي (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b5534-255">يتم دمج هذه المعلومات مع Dayforce كمجموعات دفع، ويتم فصلها حسب البلد أو المنطقة لكل دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="b5534-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b5534-256">يجب إنشاء فترة دفع واحدة على الأقل قبل الدمج.</span><span class="sxs-lookup"><span data-stu-id="b5534-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b5534-257">تقوم Dayforce بإنشاء تقويمات وتواريخ دفع للمجموعة، استنادًا إلى تاريخ بدء فترة الدفع الأولى وتاريخ الدفع الافتراضي الذي تم تحديده في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b5534-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b5534-258">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-258">Earning codes</span></span>

<span data-ttu-id="b5534-259">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b5534-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b5534-260">تحتوي أكواد الأرباح على معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b5534-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b5534-261">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b5534-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b5534-262">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-262">Earning Code (required)</span></span>
- <span data-ttu-id="b5534-263">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-263">Description</span></span>
- <span data-ttu-id="b5534-264">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="b5534-264">Unit of measure</span></span>
- <span data-ttu-id="b5534-265">منتِج</span><span class="sxs-lookup"><span data-stu-id="b5534-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b5534-266">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-266">Worker data</span></span>

<span data-ttu-id="b5534-267">تعتبر السجلات الخاصة بمختلف أنواع العاملين مهمة لأنظمة الموارد البشرية وكشوف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="b5534-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b5534-268">يمكن استخدام المعلومات التي تقوم بإدخالها لتعقب العاملين والمعلومات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="b5534-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b5534-269">يمكنك المحافظة على المعلومات التالية للعاملين:</span><span class="sxs-lookup"><span data-stu-id="b5534-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b5534-270">**أساسية** – يمكنك المحافظة على معلومات أساسية حول عامل، مثل معلومات الاتصال والمعلومات الديموغرافية ومعلومات التعريف ومعلومات حول العائلة وحالة الخدمة العسكرية ومعلومات حول المغتربين وجهات الاتصال الشخصية وجهات الاتصال عند الطوارئ.</span><span class="sxs-lookup"><span data-stu-id="b5534-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b5534-271">**التوظيف** – يمكنك المحافظة على معلومات حول توظيف العامل، مثل معلومات حول شركة أو التبعية لمؤسسة وتعيين المنصب وتاريخي البدء والانتهاء والأهلية للعمل وشروط التوظيف والمعاش والإجازة، وتغيير الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="b5534-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b5534-272">**الإجازة والغياب** – يمكنك المحافظة على معلومات حول حالات غياب العامل، مثل تقويمات العمل وحركات الغياب وإعداد الغياب.</span><span class="sxs-lookup"><span data-stu-id="b5534-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b5534-273">**التعويض وكشف المرتبات** – يمكنك المحافظة على معلومات حول خطط تعويض العامل ومعلومات كشف المرتبات، مثل التسجيل في خطة والمكافآت والأداء والعمولة ومعلومات الضريبة والتقاعد والخصومات من الراتب.</span><span class="sxs-lookup"><span data-stu-id="b5534-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b5534-274">عند إدخال معلومات العامل، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b5534-275">معلومات عامة</span><span class="sxs-lookup"><span data-stu-id="b5534-275">General information</span></span>

- <span data-ttu-id="b5534-276">رقم الموظف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-276">Personnel number (required)</span></span>
- <span data-ttu-id="b5534-277">الاسم الأول (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-277">First name (required)</span></span>
- <span data-ttu-id="b5534-278">اسم العائلة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-278">Last name (required)</span></span>
- <span data-ttu-id="b5534-279">الاسم الأوسط</span><span class="sxs-lookup"><span data-stu-id="b5534-279">Middle name</span></span>
- <span data-ttu-id="b5534-280">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="b5534-280">Seniority date</span></span>
- <span data-ttu-id="b5534-281">معروف باسم</span><span class="sxs-lookup"><span data-stu-id="b5534-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b5534-282">معلومات شخصية</span><span class="sxs-lookup"><span data-stu-id="b5534-282">Personal information</span></span>

- <span data-ttu-id="b5534-283">الحالة الاجتماعية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-283">Marital status (required)</span></span>
- <span data-ttu-id="b5534-284">تاريخ الميلاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-284">Birth date (required)</span></span>
- <span data-ttu-id="b5534-285">الجنس (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-285">Gender (required)</span></span>
- <span data-ttu-id="b5534-286">شخص معاق</span><span class="sxs-lookup"><span data-stu-id="b5534-286">Person with disabilities</span></span>
- <span data-ttu-id="b5534-287">منطقة/بلد الجنسية (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b5534-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b5534-288">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="b5534-288">Address information</span></span>

- <span data-ttu-id="b5534-289">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-289">Primary (required)</span></span>
- <span data-ttu-id="b5534-290">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-290">Country/region (required)</span></span>
- <span data-ttu-id="b5534-291">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-291">Postal code (required)</span></span>
- <span data-ttu-id="b5534-292">رقم الشارع (مطلوب) (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b5534-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b5534-293">ملحق المبنى (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b5534-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b5534-294">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-294">City (required)</span></span>
- <span data-ttu-id="b5534-295">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-295">State (required)</span></span>
- <span data-ttu-id="b5534-296">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b5534-297">معلومات الاتصال</span><span class="sxs-lookup"><span data-stu-id="b5534-297">Contact information</span></span> 

- <span data-ttu-id="b5534-298">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-298">Primary (required)</span></span>
- <span data-ttu-id="b5534-299">رقم الاتصال (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-299">Contact number (required)</span></span>
- <span data-ttu-id="b5534-300">الرقم الداخلي</span><span class="sxs-lookup"><span data-stu-id="b5534-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b5534-301">معلومات كشف المرتبات وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-301">Payroll information and earning codes</span></span>

<span data-ttu-id="b5534-302">قد يتم تعيين أرباح معينة للموظفين عند معدل تكرار دفع معين، وقد تكون لديهم طريقة دفع مفضلة.</span><span class="sxs-lookup"><span data-stu-id="b5534-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b5534-303">يتم استخدام الحقول التالية في Dayforce للمساعدة في ضمان استخدام هذه التفضيلات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="b5534-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b5534-304">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-304">Earning codes</span></span>

- <span data-ttu-id="b5534-305">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-305">Position (required)</span></span>
- <span data-ttu-id="b5534-306">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-306">Earning Code (required)</span></span>
- <span data-ttu-id="b5534-307">التكرار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-307">Frequency (required)</span></span>
- <span data-ttu-id="b5534-308">المبلغ (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b5534-309">معلومات الراتب</span><span class="sxs-lookup"><span data-stu-id="b5534-309">Payroll information</span></span>

- <span data-ttu-id="b5534-310">طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="b5534-310">Payment Method</span></span>
- <span data-ttu-id="b5534-311">المنطقة الاقتصادية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-311">Economic Region (required)</span></span>
- <span data-ttu-id="b5534-312">معرف ميزات الموظف</span><span class="sxs-lookup"><span data-stu-id="b5534-312">Employee Benefits ID</span></span>
- <span data-ttu-id="b5534-313">رقم المعرف القومي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-313">National ID Number (required)</span></span>
- <span data-ttu-id="b5534-314">رقم الخدمة العسكرية</span><span class="sxs-lookup"><span data-stu-id="b5534-314">Military Service Number</span></span>
- <span data-ttu-id="b5534-315">معرف الوردية (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-315">Shift ID (required)</span></span>
- <span data-ttu-id="b5534-316">رقم الضريبة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-316">Tax Number (required)</span></span>
- <span data-ttu-id="b5534-317">معرّف الاتحاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-317">Union ID (required)</span></span>
- <span data-ttu-id="b5534-318">معرّف يوم العمل (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-318">Work Day ID (required)</span></span>
- <span data-ttu-id="b5534-319">رقم تصريح العمل</span><span class="sxs-lookup"><span data-stu-id="b5534-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b5534-320">بالنسبة إلى طريقة الدفع، تدعم المكسيك الدفع **نقدًا** وبواسطة **شيك** (الشيك الفعلي للمؤسسة) و **الدفع الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="b5534-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b5534-321">إذا لم يتم تحديد أي طريقة دفع، فسيتم استخدام **الشيك** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="b5534-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b5534-322">تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="b5534-322">Employment details</span></span>

<span data-ttu-id="b5534-323">يتم استخدام سجل تفاصيل التوظيف كمعلومات أساسية لاستخراج حالات تعيين موظف وإنهاء خدماته وإعادة تعيينه في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b5534-324">تدعم خدمة Dayforce سجل توظيف نشط واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="b5534-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b5534-325">تاريخ بدء التوظيف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-325">Employment start date (required)</span></span>
- <span data-ttu-id="b5534-326">تاريخ انتهاء التوظيف</span><span class="sxs-lookup"><span data-stu-id="b5534-326">Employment end date</span></span>
- <span data-ttu-id="b5534-327">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="b5534-327">Start date</span></span>
- <span data-ttu-id="b5534-328">تاريخ البدء المعدل</span><span class="sxs-lookup"><span data-stu-id="b5534-328">Adjusted start date</span></span>
- <span data-ttu-id="b5534-329">تاريخ إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="b5534-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b5534-330">سبب إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="b5534-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b5534-331">يتم استخراج التواريخ الأساسية للموظف باستخدام المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="b5534-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b5534-332">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-332">Human Resources</span></span>                | <span data-ttu-id="b5534-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5534-334">أقرب تاريخ توظيف</span><span class="sxs-lookup"><span data-stu-id="b5534-334">Most recent hire date</span></span> | <span data-ttu-id="b5534-335">تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="b5534-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b5534-336">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="b5534-336">Termination date</span></span>      | <span data-ttu-id="b5534-337">تاريخ انتهاء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="b5534-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b5534-338">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="b5534-338">Start date</span></span>            | <span data-ttu-id="b5534-339">تاريخ البدء المعدل أو تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي غير النشط</span><span class="sxs-lookup"><span data-stu-id="b5534-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b5534-340">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="b5534-340">Original hire date</span></span>    | <span data-ttu-id="b5534-341">تاريخ بدء التوظيف في سجل محفوظات التوظيف الأحدث</span><span class="sxs-lookup"><span data-stu-id="b5534-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b5534-342">التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-342">Compensation</span></span>

<span data-ttu-id="b5534-343">يجب إقران خطة تعويض ثابت بالمنصب الأساسي لكل موظف خلال فترة التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b5534-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b5534-344">تبدأ هذه الفترة الزمنية في التاريخ الذي تم تعيين الموظف فيه (أو تاريخ بدء التوظيف) وتستمر حتى إنهاء خدمة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b5534-345">تاريخ السريان (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-345">Effective Date (required)</span></span>
- <span data-ttu-id="b5534-346">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b5534-346">Expiration date</span></span>
- <span data-ttu-id="b5534-347">معدل الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-347">Pay Rate (required)</span></span>
- <span data-ttu-id="b5534-348">تحويلات ‏‫معدل الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b5534-349">المكافئ السنوي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="b5534-350">المكافئ الساعي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="b5534-351">إذا كان لدى موظف ساعي مناصب متعددة، فسيتم استيراد التعويض الثابت للمنصب الأساسي إلى Dayforce كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b5534-352">فيما يتعلق بالمناصب غير الأساسية، يُحفظ المعدل الساعي إلى المنصب المناظر في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b5534-353">إذا كان لدى موظف يتلقى راتبًا مناصب متعددة، فسيتم استخراج المعدل الساعي التراكمي والراتب السنوي عبر كافة المناصب النشطة، وسيتم استخدامها كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b5534-354">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="b5534-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b5534-355">معرّف الضمان الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="b5534-355">Social Security identifier</span></span> 

<span data-ttu-id="b5534-356">يجب أن يكون لدى كل موظف معرّفًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="b5534-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b5534-357">يجب أن يكون هذا المعرّف من نوع التعريف‬ **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b5534-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b5534-358">في Dayforce، يتم استخراجه تلقائيًا على أنه معرّف الضمان الاجتماعي للموظف المطلوب للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="b5534-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b5534-359">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-359">Primary (required)</span></span>
- <span data-ttu-id="b5534-360">نوع التعريف = "SSN"</span><span class="sxs-lookup"><span data-stu-id="b5534-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b5534-361">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="b5534-361">Issued Date</span></span>
- <span data-ttu-id="b5534-362">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b5534-362">Expiration Date</span></span>

<span data-ttu-id="b5534-363">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b5534-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b5534-364">ومع ذلك، فإن السجل الذي سيتم دمجه في Dayforce هو فقط الذي يحمل العلامة **أساسي**، بصرف النظر عما إذا كان الرقم نشطًا أو منتهي الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="b5534-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b5534-365">الحسابات البنكية والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="b5534-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="b5534-366">يجب إدخال معلومات صالحة حول الحساب البنكي لأي موظف يختار تلقي الدفع من خلال تحويلات إلى الحساب البنكي‬.</span><span class="sxs-lookup"><span data-stu-id="b5534-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b5534-367">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-367">Human Resources</span></span>                         | <span data-ttu-id="b5534-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5534-369">رقم الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b5534-370">رمز SWIFT (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-370">SWIFT code (required)</span></span>          | <span data-ttu-id="b5534-371">حقل **معرّف البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b5534-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b5534-372">رقم الفرع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b5534-373">نوع الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-373">Bank account type (required)</span></span>   | <span data-ttu-id="b5534-374">حقل **نوع البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b5534-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b5534-375">تتضمن القيم المدعومة **شيكات** و **كشف المرتبات**.</span><span class="sxs-lookup"><span data-stu-id="b5534-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b5534-376">يتعين على الموظفين الذين اختاروا تلقي الدفع عبر تحويلات إلى الحساب البنكي‬ توفير ارتباط إلى حساب متبقٍ موجود ضمن كيان قانوني عنوانه الأساسي في المكسيك ويقترن بحساب بنكي صالح من بنك مكسيكي.</span><span class="sxs-lookup"><span data-stu-id="b5534-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b5534-377">يتم تجاهل كافة الحسابات الأخرى غير الحسابات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b5534-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b5534-378">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="b5534-378">Address information</span></span>

<span data-ttu-id="b5534-379">يجب أن يكون لدى كل موظف موقعًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="b5534-379">Every employee must have one primary location.</span></span> <span data-ttu-id="b5534-380">في Dayforce، يتم استخدام هذا الموقع لتحديد مكان الإقامة الأساسي للموظف لأغراض ضريبية.</span><span class="sxs-lookup"><span data-stu-id="b5534-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b5534-381">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-381">Primary (required)</span></span>
- <span data-ttu-id="b5534-382">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-382">Country/region (required)</span></span>
- <span data-ttu-id="b5534-383">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="b5534-384">الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-384">Street (required)</span></span>
- <span data-ttu-id="b5534-385">رقم الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-385">Street Number (required)</span></span>
- <span data-ttu-id="b5534-386">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="b5534-386">Building Complement</span></span>
- <span data-ttu-id="b5534-387">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-387">City (required)</span></span>
- <span data-ttu-id="b5534-388">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-388">State (required)</span></span>
- <span data-ttu-id="b5534-389">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b5534-390">تكوين البيانات لإنشاء كشف مرتبات في الولايات المتحدة وكندا</span><span class="sxs-lookup"><span data-stu-id="b5534-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b5534-391">إذا كنت تقوم بإنشاء الدفع للموظفين في الولايات المتحدة وكندا، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b5534-392">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="b5534-392">Departments are required on positions.</span></span>
- <span data-ttu-id="b5534-393">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b5534-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="b5534-394">يمكنك تكوين لـ Human Resourcesمطالبة المناصب بتحديد قسم.</span><span class="sxs-lookup"><span data-stu-id="b5534-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="b5534-395">للقيام بذلك، انتقل إلى **الموارد البشرية المناصب المشتركة > المناصب > الأقسام مطلوبة على المناصب**.</span><span class="sxs-lookup"><span data-stu-id="b5534-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="b5534-396">من المستحسن أن يتم فرض هذا الإعداد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="b5534-397">أنواع الوظائف</span><span class="sxs-lookup"><span data-stu-id="b5534-397">Job types</span></span>

<span data-ttu-id="b5534-398">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="b5534-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b5534-399">تعتبر أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في الولايات المتحدة وكندا.</span><span class="sxs-lookup"><span data-stu-id="b5534-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b5534-400">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="b5534-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b5534-401">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="b5534-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b5534-402">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b5534-403">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b5534-403">Job type</span></span>   | <span data-ttu-id="b5534-404">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b5534-405">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b5534-405">Hourly</span></span>     | <span data-ttu-id="b5534-406">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b5534-406">Hourly</span></span>      |
| <span data-ttu-id="b5534-407">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b5534-407">Salaried</span></span>   | <span data-ttu-id="b5534-408">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b5534-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b5534-409">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="b5534-409">Position types</span></span> 

<span data-ttu-id="b5534-410">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="b5534-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b5534-411">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="b5534-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b5534-412">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b5534-413">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="b5534-413">Position type</span></span>   | <span data-ttu-id="b5534-414">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b5534-415">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="b5534-415">Full-time</span></span>       | <span data-ttu-id="b5534-416">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="b5534-416">Full time employee</span></span> |
| <span data-ttu-id="b5534-417">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b5534-417">Part-time</span></span>       | <span data-ttu-id="b5534-418">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b5534-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b5534-419">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="b5534-419">Reason codes</span></span>

<span data-ttu-id="b5534-420">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b5534-421">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="b5534-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b5534-422">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b5534-423">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="b5534-423">Reason code</span></span>    | <span data-ttu-id="b5534-424">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-424">Description</span></span>      | <span data-ttu-id="b5534-425">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b5534-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b5534-426">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b5534-426">RESIGNATION</span></span>    | <span data-ttu-id="b5534-427">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b5534-427">Resignation</span></span>      | <span data-ttu-id="b5534-428">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-428">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-429">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b5534-429">TERMINATION</span></span>    | <span data-ttu-id="b5534-430">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b5534-430">Termination</span></span>      | <span data-ttu-id="b5534-431">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-431">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-432">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b5534-432">RETIREMENT</span></span>     | <span data-ttu-id="b5534-433">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b5534-433">Retirement</span></span>       | <span data-ttu-id="b5534-434">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-434">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-435">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b5534-435">OTHER</span></span>          | <span data-ttu-id="b5534-436">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="b5534-436">Other Reasons</span></span>    | <span data-ttu-id="b5534-437">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-437">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-438">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b5534-438">DEATH</span></span>          | <span data-ttu-id="b5534-439">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b5534-439">Death</span></span>            | <span data-ttu-id="b5534-440">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-440">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b5534-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b5534-442">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="b5534-442">Leave of Absence</span></span> | <span data-ttu-id="b5534-443">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-443">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b5534-444">CONTRACTEND</span></span>    | <span data-ttu-id="b5534-445">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="b5534-445">End of Contract</span></span>  | <span data-ttu-id="b5534-446">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-446">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b5534-447">SALARYCHANGE</span></span>   | <span data-ttu-id="b5534-448">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="b5534-448">Change of Salary</span></span> | <span data-ttu-id="b5534-449">التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b5534-450">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="b5534-450">Marital status</span></span>

<span data-ttu-id="b5534-451">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b5534-452">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b5534-453">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-453">Human Resources</span></span>                 | <span data-ttu-id="b5534-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b5534-455">متزوج</span><span class="sxs-lookup"><span data-stu-id="b5534-455">Married</span></span>                | <span data-ttu-id="b5534-456">متزوج</span><span class="sxs-lookup"><span data-stu-id="b5534-456">Married</span></span>              |
| <span data-ttu-id="b5534-457">أعزب</span><span class="sxs-lookup"><span data-stu-id="b5534-457">Single</span></span>                 | <span data-ttu-id="b5534-458">أعزب</span><span class="sxs-lookup"><span data-stu-id="b5534-458">Single</span></span>               |
| <span data-ttu-id="b5534-459">أرمل</span><span class="sxs-lookup"><span data-stu-id="b5534-459">Widowed</span></span>                | <span data-ttu-id="b5534-460">أرمل</span><span class="sxs-lookup"><span data-stu-id="b5534-460">Widowed</span></span>              |
| <span data-ttu-id="b5534-461">مطلق</span><span class="sxs-lookup"><span data-stu-id="b5534-461">Divorced</span></span>               | <span data-ttu-id="b5534-462">مطلق</span><span class="sxs-lookup"><span data-stu-id="b5534-462">Divorced</span></span>             |
| <span data-ttu-id="b5534-463">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="b5534-463">Registered Partnership</span></span> | <span data-ttu-id="b5534-464">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="b5534-464">Domestic Partnership</span></span> |
| <span data-ttu-id="b5534-465">بلا</span><span class="sxs-lookup"><span data-stu-id="b5534-465">None</span></span>                   | <span data-ttu-id="b5534-466">بلا</span><span class="sxs-lookup"><span data-stu-id="b5534-466">None</span></span>                 |
| <span data-ttu-id="b5534-467">تعايش</span><span class="sxs-lookup"><span data-stu-id="b5534-467">Cohabiting</span></span>             | <span data-ttu-id="b5534-468">تعايش</span><span class="sxs-lookup"><span data-stu-id="b5534-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b5534-469">الجنس</span><span class="sxs-lookup"><span data-stu-id="b5534-469">Gender</span></span>

<span data-ttu-id="b5534-470">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b5534-471">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b5534-472">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-472">Human Resources</span></span>       | <span data-ttu-id="b5534-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b5534-474">ذكر</span><span class="sxs-lookup"><span data-stu-id="b5534-474">Male</span></span>         | <span data-ttu-id="b5534-475">ذكر</span><span class="sxs-lookup"><span data-stu-id="b5534-475">Male</span></span>            |
| <span data-ttu-id="b5534-476">أنثى</span><span class="sxs-lookup"><span data-stu-id="b5534-476">Female</span></span>       | <span data-ttu-id="b5534-477">أنثى</span><span class="sxs-lookup"><span data-stu-id="b5534-477">Female</span></span>          |
| <span data-ttu-id="b5534-478">غير محدد</span><span class="sxs-lookup"><span data-stu-id="b5534-478">Non-specific</span></span> | <span data-ttu-id="b5534-479">*غير مدعوم*</span><span class="sxs-lookup"><span data-stu-id="b5534-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b5534-480">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-480">Earning codes</span></span>

<span data-ttu-id="b5534-481">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b5534-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b5534-482">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b5534-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b5534-483">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="b5534-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b5534-484">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b5534-484">Supported frequencies</span></span>

- <span data-ttu-id="b5534-485">الكل</span><span class="sxs-lookup"><span data-stu-id="b5534-485">All</span></span>
- <span data-ttu-id="b5534-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b5534-486">EVERYPAY</span></span>
- <span data-ttu-id="b5534-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b5534-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b5534-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b5534-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b5534-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b5534-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b5534-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-490">1OFMTH</span></span>
- <span data-ttu-id="b5534-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-491">LASTOFMTH</span></span>
- <span data-ttu-id="b5534-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-492">2OFMTH</span></span>
- <span data-ttu-id="b5534-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-493">3OFMTH</span></span>
- <span data-ttu-id="b5534-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-494">4OFMTH</span></span>
- <span data-ttu-id="b5534-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-495">5OFMTH</span></span>
- <span data-ttu-id="b5534-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-496">1N2OFMTH</span></span>
- <span data-ttu-id="b5534-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-497">3N4OFMTH</span></span>
- <span data-ttu-id="b5534-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-498">1N3OFMTH</span></span>
- <span data-ttu-id="b5534-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-499">1N4OFMTH</span></span>
- <span data-ttu-id="b5534-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-500">2N3OFMTH</span></span>
- <span data-ttu-id="b5534-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-501">2N4OFMTH</span></span>
- <span data-ttu-id="b5534-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="b5534-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="b5534-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b5534-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b5534-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b5534-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b5534-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b5534-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b5534-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b5534-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b5534-514">العناوين</span><span class="sxs-lookup"><span data-stu-id="b5534-514">Addresses</span></span>

<span data-ttu-id="b5534-515">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="b5534-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b5534-516">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="b5534-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b5534-517">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-517">Human Resources</span></span>          | <span data-ttu-id="b5534-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b5534-519">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="b5534-519">Country/Region</span></span>  | <span data-ttu-id="b5534-520">كود البلد</span><span class="sxs-lookup"><span data-stu-id="b5534-520">Country Code</span></span>          |
| <span data-ttu-id="b5534-521">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b5534-521">Zip/Postal Code</span></span> | <span data-ttu-id="b5534-522">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b5534-522">Postal Code</span></span>           |
| <span data-ttu-id="b5534-523">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="b5534-523">State</span></span>           | <span data-ttu-id="b5534-524">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="b5534-524">State Code</span></span>            |
| <span data-ttu-id="b5534-525">المدينة</span><span class="sxs-lookup"><span data-stu-id="b5534-525">City</span></span>            | <span data-ttu-id="b5534-526">المدينة</span><span class="sxs-lookup"><span data-stu-id="b5534-526">City</span></span>                  |
| <span data-ttu-id="b5534-527">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b5534-527">County</span></span>          | <span data-ttu-id="b5534-528">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="b5534-528">County (Municipality)</span></span> |
| <span data-ttu-id="b5534-529">الشارع</span><span class="sxs-lookup"><span data-stu-id="b5534-529">Street</span></span>          | <span data-ttu-id="b5534-530">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="b5534-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b5534-531">مناطق الضريبة</span><span class="sxs-lookup"><span data-stu-id="b5534-531">Tax regions</span></span>

<span data-ttu-id="b5534-532">تُستخدم مناطق الضريبة لتحديد الضريبة المناسبة التي يجب تطبيقها أثناء إنشاء كشف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="b5534-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b5534-533">يتم تعيين مناطق الضريبة إلى Dayforce كعناوين موقع.</span><span class="sxs-lookup"><span data-stu-id="b5534-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b5534-534">يجب أن تكون منطقة الضريبة الافتراضية مقترنة بمنصب العامل النشط.</span><span class="sxs-lookup"><span data-stu-id="b5534-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b5534-535">منطقة الضريبة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-535">Tax region (required)</span></span>
- <span data-ttu-id="b5534-536">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b5534-536">Country/Region (required)</span></span>
- <span data-ttu-id="b5534-537">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-537">State (required)</span></span>
- <span data-ttu-id="b5534-538">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b5534-538">County</span></span> 
- <span data-ttu-id="b5534-539">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b5534-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b5534-540">تكوين بياناتك لإنشاء كشف المرتبات في المكسيك</span><span class="sxs-lookup"><span data-stu-id="b5534-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b5534-541">إذا كنت تقوم بإنشاء الدفع للموظفين في المكسيك، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b5534-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b5534-542">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="b5534-542">Departments are required on positions.</span></span>
- <span data-ttu-id="b5534-543">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b5534-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b5534-544">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b5534-544">Job types</span></span>

<span data-ttu-id="b5534-545">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="b5534-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b5534-546">أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b5534-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b5534-547">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="b5534-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b5534-548">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="b5534-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b5534-549">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b5534-550">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b5534-550">Job type</span></span>   | <span data-ttu-id="b5534-551">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b5534-552">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b5534-552">Hourly</span></span>     | <span data-ttu-id="b5534-553">الحد الأقصى للأجر في الساعة‬</span><span class="sxs-lookup"><span data-stu-id="b5534-553">MX Hourly</span></span>   |
| <span data-ttu-id="b5534-554">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b5534-554">Salaried</span></span>   | <span data-ttu-id="b5534-555">الحد الأقصى للراتب</span><span class="sxs-lookup"><span data-stu-id="b5534-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b5534-556">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="b5534-556">Position types</span></span> 

<span data-ttu-id="b5534-557">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="b5534-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b5534-558">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="b5534-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b5534-559">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b5534-560">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="b5534-560">Position type</span></span>   | <span data-ttu-id="b5534-561">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b5534-562">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="b5534-562">Full-time</span></span>       | <span data-ttu-id="b5534-563">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="b5534-563">Full time employee</span></span> |
| <span data-ttu-id="b5534-564">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b5534-564">Part-time</span></span>       | <span data-ttu-id="b5534-565">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b5534-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b5534-566">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="b5534-566">Reason codes</span></span>

<span data-ttu-id="b5534-567">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b5534-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b5534-568">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="b5534-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b5534-569">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b5534-570">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="b5534-570">Reason code</span></span>            | <span data-ttu-id="b5534-571">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-571">Description</span></span>                    | <span data-ttu-id="b5534-572">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b5534-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b5534-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b5534-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b5534-574">المغادرة قبل كشف المرتبات الأول</span><span class="sxs-lookup"><span data-stu-id="b5534-574">Departure before first payroll</span></span> | <span data-ttu-id="b5534-575">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-575">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-576">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b5534-576">RESIGNATION</span></span>            | <span data-ttu-id="b5534-577">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b5534-577">Resignation</span></span>                    | <span data-ttu-id="b5534-578">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-578">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-579">المعاش</span><span class="sxs-lookup"><span data-stu-id="b5534-579">PENSION</span></span>                | <span data-ttu-id="b5534-580">المعاش</span><span class="sxs-lookup"><span data-stu-id="b5534-580">Pension</span></span>                        | <span data-ttu-id="b5534-581">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-581">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-582">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b5534-582">TERMINATION</span></span>            | <span data-ttu-id="b5534-583">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b5534-583">Termination</span></span>                    | <span data-ttu-id="b5534-584">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-584">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-585">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b5534-585">RETIREMENT</span></span>             | <span data-ttu-id="b5534-586">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b5534-586">Retirement</span></span>                     | <span data-ttu-id="b5534-587">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-587">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-588">الغائب</span><span class="sxs-lookup"><span data-stu-id="b5534-588">ABSENTEE</span></span>               | <span data-ttu-id="b5534-589">الغائب</span><span class="sxs-lookup"><span data-stu-id="b5534-589">Absentee</span></span>                       | <span data-ttu-id="b5534-590">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-590">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-591">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b5534-591">OTHER</span></span>                  | <span data-ttu-id="b5534-592">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="b5534-592">Other Reasons</span></span>                  | <span data-ttu-id="b5534-593">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-593">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-594">إقفال</span><span class="sxs-lookup"><span data-stu-id="b5534-594">CLOSURE</span></span>                | <span data-ttu-id="b5534-595">إقفال الشركة</span><span class="sxs-lookup"><span data-stu-id="b5534-595">Business Closure</span></span>               | <span data-ttu-id="b5534-596">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-596">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-597">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b5534-597">DEATH</span></span>                  | <span data-ttu-id="b5534-598">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b5534-598">Death</span></span>                          | <span data-ttu-id="b5534-599">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-599">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b5534-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b5534-601">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="b5534-601">Leave of Absence</span></span>               | <span data-ttu-id="b5534-602">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-602">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b5534-603">CONTRACTEND</span></span>            | <span data-ttu-id="b5534-604">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="b5534-604">End of Contract</span></span>                | <span data-ttu-id="b5534-605">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b5534-605">Terminate worker</span></span>     |
| <span data-ttu-id="b5534-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b5534-606">SALARYCHANGE</span></span>           | <span data-ttu-id="b5534-607">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="b5534-607">Change of Salary</span></span>               | <span data-ttu-id="b5534-608">التعويض</span><span class="sxs-lookup"><span data-stu-id="b5534-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b5534-609">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="b5534-609">Terms of employment</span></span>

<span data-ttu-id="b5534-610">يتم استخدام شروط التوظيف لإنشاء فئات شروط التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b5534-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b5534-611">يتم تعيين الشروط إلى Dayforce كقيم مؤشر التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b5534-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b5534-612">شروط التوظيف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5534-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b5534-613">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="b5534-613">Terms of employment</span></span>   | <span data-ttu-id="b5534-614">الوصف</span><span class="sxs-lookup"><span data-stu-id="b5534-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b5534-615">عادي</span><span class="sxs-lookup"><span data-stu-id="b5534-615">Regular</span></span>               | <span data-ttu-id="b5534-616">عادي</span><span class="sxs-lookup"><span data-stu-id="b5534-616">Regular</span></span>     |
| <span data-ttu-id="b5534-617">مباشر</span><span class="sxs-lookup"><span data-stu-id="b5534-617">Direct</span></span>                | <span data-ttu-id="b5534-618">مباشر</span><span class="sxs-lookup"><span data-stu-id="b5534-618">Direct</span></span>      |
| <span data-ttu-id="b5534-619">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="b5534-619">Internship</span></span>            | <span data-ttu-id="b5534-620">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="b5534-620">Internship</span></span>  |
| <span data-ttu-id="b5534-621">دائم</span><span class="sxs-lookup"><span data-stu-id="b5534-621">Permanent</span></span>             | <span data-ttu-id="b5534-622">دائم</span><span class="sxs-lookup"><span data-stu-id="b5534-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b5534-623">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="b5534-623">Marital status</span></span>

<span data-ttu-id="b5534-624">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b5534-625">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b5534-626">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-626">Human Resources</span></span>                 | <span data-ttu-id="b5534-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b5534-628">متزوج</span><span class="sxs-lookup"><span data-stu-id="b5534-628">Married</span></span>                | <span data-ttu-id="b5534-629">متزوج</span><span class="sxs-lookup"><span data-stu-id="b5534-629">Married</span></span>                   |
| <span data-ttu-id="b5534-630">أعزب</span><span class="sxs-lookup"><span data-stu-id="b5534-630">Single</span></span>                 | <span data-ttu-id="b5534-631">أعزب</span><span class="sxs-lookup"><span data-stu-id="b5534-631">Single</span></span>                    |
| <span data-ttu-id="b5534-632">أرمل</span><span class="sxs-lookup"><span data-stu-id="b5534-632">Widowed</span></span>                | <span data-ttu-id="b5534-633">أرمل</span><span class="sxs-lookup"><span data-stu-id="b5534-633">Widowed</span></span>                   |
| <span data-ttu-id="b5534-634">مطلق</span><span class="sxs-lookup"><span data-stu-id="b5534-634">Divorced</span></span>               | <span data-ttu-id="b5534-635">مطلق</span><span class="sxs-lookup"><span data-stu-id="b5534-635">Divorced</span></span>                  |
| <span data-ttu-id="b5534-636">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="b5534-636">Registered Partnership</span></span> | <span data-ttu-id="b5534-637">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="b5534-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="b5534-638">بلا</span><span class="sxs-lookup"><span data-stu-id="b5534-638">None</span></span>                   | <span data-ttu-id="b5534-639">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b5534-640">تعايش</span><span class="sxs-lookup"><span data-stu-id="b5534-640">Cohabiting</span></span>             | <span data-ttu-id="b5534-641">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b5534-642">الجنس</span><span class="sxs-lookup"><span data-stu-id="b5534-642">Gender</span></span>

<span data-ttu-id="b5534-643">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b5534-644">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b5534-645">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-645">Human Resources</span></span>       | <span data-ttu-id="b5534-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b5534-647">ذكر</span><span class="sxs-lookup"><span data-stu-id="b5534-647">Male</span></span>         | <span data-ttu-id="b5534-648">ذكر</span><span class="sxs-lookup"><span data-stu-id="b5534-648">Male</span></span>                      |
| <span data-ttu-id="b5534-649">أنثى</span><span class="sxs-lookup"><span data-stu-id="b5534-649">Female</span></span>       | <span data-ttu-id="b5534-650">أنثى</span><span class="sxs-lookup"><span data-stu-id="b5534-650">Female</span></span>                    |
| <span data-ttu-id="b5534-651">غير محدد</span><span class="sxs-lookup"><span data-stu-id="b5534-651">Non-specific</span></span> | <span data-ttu-id="b5534-652">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b5534-653">أسلوب الدفع</span><span class="sxs-lookup"><span data-stu-id="b5534-653">Payment method</span></span>

<span data-ttu-id="b5534-654">تقدم طرق دفع للموظف والشركة طريقة لوصف كيفية تسديد مرتبات وأجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="b5534-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b5534-655">يتم تعيين طرق الدفع إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b5534-656">يعرض الجدول التالي كيفية تعيين طرق الدفع إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b5534-657">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-657">Human Resources</span></span>             | <span data-ttu-id="b5534-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b5534-659">نقدي</span><span class="sxs-lookup"><span data-stu-id="b5534-659">Cash</span></span>               | <span data-ttu-id="b5534-660">نقدي</span><span class="sxs-lookup"><span data-stu-id="b5534-660">Cash</span></span>                      |
| <span data-ttu-id="b5534-661">دفع إلكتروني</span><span class="sxs-lookup"><span data-stu-id="b5534-661">Electronic Payment</span></span> | <span data-ttu-id="b5534-662">التحويل</span><span class="sxs-lookup"><span data-stu-id="b5534-662">Transfer</span></span>                  |
| <span data-ttu-id="b5534-663">فحص</span><span class="sxs-lookup"><span data-stu-id="b5534-663">Check</span></span>              | <span data-ttu-id="b5534-664">شيك</span><span class="sxs-lookup"><span data-stu-id="b5534-664">Cheque</span></span>                    |
| <span data-ttu-id="b5534-665">حوالة مصرفية</span><span class="sxs-lookup"><span data-stu-id="b5534-665">Bank Draft</span></span>         | <span data-ttu-id="b5534-666">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b5534-667">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b5534-667">Other</span></span>              | <span data-ttu-id="b5534-668">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b5534-669">نوع الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="b5534-669">Bank account type</span></span>

<span data-ttu-id="b5534-670">يتم استخدام أنواع الحسابات البنكية للدفع الإلكتروني للموظفين.</span><span class="sxs-lookup"><span data-stu-id="b5534-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b5534-671">يتم تعيين أنواع الحسابات البنكية إلى Dayforce كمعلومات حساب التحويل.</span><span class="sxs-lookup"><span data-stu-id="b5534-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b5534-672">وتتم ترجمة أنواع الحسابات البنكية، كما هو مناسب، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b5534-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b5534-673">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-673">Human Resources</span></span>            | <span data-ttu-id="b5534-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b5534-675">حساب شيكات</span><span class="sxs-lookup"><span data-stu-id="b5534-675">Checking Account</span></span>  | <span data-ttu-id="b5534-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="b5534-676">CheckingAccount</span></span>           |
| <span data-ttu-id="b5534-677">حساب الراتب</span><span class="sxs-lookup"><span data-stu-id="b5534-677">Payroll Account</span></span>   | <span data-ttu-id="b5534-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b5534-678">PayrollAccount</span></span>            |
| <span data-ttu-id="b5534-679">حساب توفير</span><span class="sxs-lookup"><span data-stu-id="b5534-679">Savings Account</span></span>   | <span data-ttu-id="b5534-680">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b5534-681">حساب BankGirot</span><span class="sxs-lookup"><span data-stu-id="b5534-681">BankGirot account</span></span> | <span data-ttu-id="b5534-682">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b5534-683">حساب PlusGirot</span><span class="sxs-lookup"><span data-stu-id="b5534-683">PlusGirot account</span></span> | <span data-ttu-id="b5534-684">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b5534-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b5534-685">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b5534-685">Earning codes</span></span>

<span data-ttu-id="b5534-686">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b5534-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b5534-687">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b5534-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b5534-688">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="b5534-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b5534-689">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b5534-689">Supported frequencies</span></span>

- <span data-ttu-id="b5534-690">الكل</span><span class="sxs-lookup"><span data-stu-id="b5534-690">All</span></span>
- <span data-ttu-id="b5534-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b5534-691">EVERYPAY</span></span>
- <span data-ttu-id="b5534-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b5534-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b5534-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b5534-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b5534-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b5534-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b5534-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-695">1OFMTH</span></span>
- <span data-ttu-id="b5534-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-696">LASTOFMTH</span></span>
- <span data-ttu-id="b5534-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-697">2OFMTH</span></span>
- <span data-ttu-id="b5534-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-698">3OFMTH</span></span>
- <span data-ttu-id="b5534-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-699">4OFMTH</span></span>
- <span data-ttu-id="b5534-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-700">5OFMTH</span></span>
- <span data-ttu-id="b5534-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-701">1N2OFMTH</span></span>
- <span data-ttu-id="b5534-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-702">3N4OFMTH</span></span>
- <span data-ttu-id="b5534-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-703">1N3OFMTH</span></span>
- <span data-ttu-id="b5534-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-704">1N4OFMTH</span></span>
- <span data-ttu-id="b5534-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-705">2N3OFMTH</span></span>
- <span data-ttu-id="b5534-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-706">2N4OFMTH</span></span>
- <span data-ttu-id="b5534-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="b5534-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="b5534-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b5534-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b5534-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b5534-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b5534-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b5534-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b5534-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b5534-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b5534-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b5534-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b5534-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b5534-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b5534-719">العناوين</span><span class="sxs-lookup"><span data-stu-id="b5534-719">Addresses</span></span>

<span data-ttu-id="b5534-720">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="b5534-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b5534-721">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="b5534-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b5534-722">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b5534-722">Human Resources</span></span>              | <span data-ttu-id="b5534-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b5534-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b5534-724">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="b5534-724">Country/Region</span></span>      | <span data-ttu-id="b5534-725">كود البلد</span><span class="sxs-lookup"><span data-stu-id="b5534-725">Country Code</span></span>          |
| <span data-ttu-id="b5534-726">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b5534-726">Zip/Postal Code</span></span>     | <span data-ttu-id="b5534-727">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b5534-727">Postal Code</span></span>           |
| <span data-ttu-id="b5534-728">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="b5534-728">State</span></span>               | <span data-ttu-id="b5534-729">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="b5534-729">State Code</span></span>            |
| <span data-ttu-id="b5534-730">المدينة</span><span class="sxs-lookup"><span data-stu-id="b5534-730">City</span></span>                | <span data-ttu-id="b5534-731">المدينة</span><span class="sxs-lookup"><span data-stu-id="b5534-731">City</span></span>                  |
| <span data-ttu-id="b5534-732">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b5534-732">County</span></span>              | <span data-ttu-id="b5534-733">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="b5534-733">County (Municipality)</span></span> |
| <span data-ttu-id="b5534-734">الشارع</span><span class="sxs-lookup"><span data-stu-id="b5534-734">Street</span></span>              | <span data-ttu-id="b5534-735">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="b5534-735">Address Line 1</span></span>        |
| <span data-ttu-id="b5534-736">رقم الشارع</span><span class="sxs-lookup"><span data-stu-id="b5534-736">Street Number</span></span>       | <span data-ttu-id="b5534-737">سطر العنوان 2</span><span class="sxs-lookup"><span data-stu-id="b5534-737">Address Line 2</span></span>        |
| <span data-ttu-id="b5534-738">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="b5534-738">Building Complement</span></span> | <span data-ttu-id="b5534-739">سطر العنوان 5</span><span class="sxs-lookup"><span data-stu-id="b5534-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b5534-740">رقم جواز السفر</span><span class="sxs-lookup"><span data-stu-id="b5534-740">Passport number</span></span>

<span data-ttu-id="b5534-741">بإمكان الموظفين إعلان معلومات جواز السفر.</span><span class="sxs-lookup"><span data-stu-id="b5534-741">Employees can declare passport information.</span></span> <span data-ttu-id="b5534-742">هذه المعلومات هي نوع من أنواع تعريف **جواز السفر** وهي تتكامل في Dayforce كجزء من معلومات الموظف خاصة بالمكسيك.</span><span class="sxs-lookup"><span data-stu-id="b5534-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b5534-743">نوع التعريف = "جواز سفر"</span><span class="sxs-lookup"><span data-stu-id="b5534-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b5534-744">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="b5534-744">Issued Date</span></span>
- <span data-ttu-id="b5534-745">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b5534-745">Expiration Date</span></span>

<span data-ttu-id="b5534-746">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **جواز سفر**.</span><span class="sxs-lookup"><span data-stu-id="b5534-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b5534-747">ومع ذلك، يتم دمج إدخال جواز السفر النشط الحالي فقط في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b5534-748">إذا انتهت صلاحية جميع إدخالات جوازات السفر، فسيتكامل جواز السفر الذي تم إصداره مؤخرًا في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b5534-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]