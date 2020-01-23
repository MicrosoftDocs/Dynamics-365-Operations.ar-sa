---
title: تكوين تكامل كشف المرتبات بين Talent وDayforce
description: يشرح هذا الموضوع كيفية تكوين التكامل بين Microsoft Dynamics 365 Talent وCeridian Dayforce لكي تتمكن من معالجة دورة دفع.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898516"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="791f4-103">تكوين تكامل الرواتب بين Talent وDayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="791f4-104">يعتمد التكامل بين Dynamics 365 Talent وCeridian Dayforce على العديد من خطوات التكوين التي تم وصفها في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="791f4-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="791f4-105">يجب عليك تكوين التكامل في كل من Talent وDayforce قبل أن تتمكن من معالجة دورة دفع.</span><span class="sxs-lookup"><span data-stu-id="791f4-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="791f4-106">عندما تستخدم خدمة مثل Dayforce لإتمام دورات الدفع، يجب عليك تمكين التكامل في Talent.</span><span class="sxs-lookup"><span data-stu-id="791f4-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="791f4-107">يتطلب التكامل بيانات معينة من Talent.</span><span class="sxs-lookup"><span data-stu-id="791f4-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="791f4-108">لذلك، يجب عليك التأكد من أن البيانات التي تم تعيينها إلى Dayforce هي بيانات تم تكوينها في Talent بطريقة تدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="791f4-109">يستخدم التكامل الفئات الواسعة التالية من البيانات:</span><span class="sxs-lookup"><span data-stu-id="791f4-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="791f4-110">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="791f4-110">Human resources data</span></span>
- <span data-ttu-id="791f4-111">بيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-111">Compensation data</span></span>
- <span data-ttu-id="791f4-112">بيانات كشف المرتبات، مثل دورات الدفع وفترات الدفع وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="791f4-113">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-113">Worker data</span></span>

<span data-ttu-id="791f4-114">يصف هذا الموضوع الخطوات التي يجب اتباعها لتمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="791f4-115">ويشرح أيضًا أنواع البيانات وتفاصيل التكوين التي يحتاج إليها التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="791f4-116">تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="791f4-116">Enable the integration</span></span>

<span data-ttu-id="791f4-117">في Talent، يجب تشغيل التكامل وإدخال معلومات التكوين للاتصال بخدمة Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="791f4-118">إذا أردت أن يتم استيراد حركة دفتر الأستاذ العام التي نشأت إلى Microsoft Dynamics 365 Finance، فيجب أيضًا إعداد حساب تخزين في Microsoft Azure وإدخال سلسلة اتصال Azure Storage في Finance.</span><span class="sxs-lookup"><span data-stu-id="791f4-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="791f4-119">لتشغيل التكامل في Talent، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="791f4-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="791f4-120">في صفحة **إدارة النظام**، حدد **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="791f4-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="791f4-121">أدخل نقطة نهاية بروتوكول نقل الملفات (FTP) الآمنة ومسار مجلد FTP الآمن.</span><span class="sxs-lookup"><span data-stu-id="791f4-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="791f4-122">أدخل اسم المستخدم وكلمة المرور للمستخدم الذي سينتقل إلى نقطة النهاية الآمنة ومسار المجلد الآمن في بروتوكول FTP.</span><span class="sxs-lookup"><span data-stu-id="791f4-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="791f4-123">اختبر الاتصال، كما تقتضي الحاجة، وعيّن الخيار **تمكين تكامل كشف المرتبات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="791f4-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="791f4-124">عند تشغيل التكامل، يتم إنشاء حزمة وملفات تصدير البيانات ويتم تعيين معدل التكرار.</span><span class="sxs-lookup"><span data-stu-id="791f4-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="791f4-125">ويمكنك تغيير معدل التكرار وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="791f4-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="791f4-126">لمزيد من المعلومات حول حسابات مساحة تخزين Azure وسلاسل اتصال مساحة تخزين Azure، راجع موضوعات Azure التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="791f4-127">حول حسابات مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="791f4-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="791f4-128">تكوين سلاسل اتصال مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="791f4-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="791f4-129">تفاصيل تقنية عند تمكين تكامل الرواتب</span><span class="sxs-lookup"><span data-stu-id="791f4-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="791f4-130">يؤدي تشغيل تكامل الرواتب إلى تأثيرين أساسيين:</span><span class="sxs-lookup"><span data-stu-id="791f4-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="791f4-131">يتم إنشاء مشروع تصدير بيانات يُسمى "تصدير تكامل الرواتب".</span><span class="sxs-lookup"><span data-stu-id="791f4-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="791f4-132">يحتوي هذا المشروع على الكيانات والحقول المطلوبة لتكامل الرواتب.</span><span class="sxs-lookup"><span data-stu-id="791f4-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="791f4-133">لفحص المشروع، انتقل إلى **إدارة النظام**، وحدد تجانب**إدارة البيانات**، ثم افتح مشروع البيانات من قائمة المشروعات.</span><span class="sxs-lookup"><span data-stu-id="791f4-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="791f4-134">تنفذ هذه الوظيفة الدفعية مشروع تصدير البيانات، وتشفر حزمة البيانات الناتجة، وتنقل ملف حزمة البيانات إلى نقطة نهاية SFTP التي تم تكوينها على شاشة **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="791f4-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="791f4-135">يتم تشفير حزمة البيانات التي تم نقلها إلى نقطة نهاية SFTP باستخدام مفتاح فريد للحزمة.</span><span class="sxs-lookup"><span data-stu-id="791f4-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="791f4-136">المفتاح موجود في Azure Key Vault والذي يمكن الوصول إليه عن طريق Ceridian فقط.</span><span class="sxs-lookup"><span data-stu-id="791f4-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="791f4-137">لا يمكن فك تشفير محتويات حزمة البيانات وفحصها.</span><span class="sxs-lookup"><span data-stu-id="791f4-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="791f4-138">إذا كنت بحاجة إلى فحص محتويات حزمة البيانات، ستحتاج إلى تصدير مشروع البيانات "تصدير تكامل الرواتب" يدويا، وتنزيله، ثم فتحه.</span><span class="sxs-lookup"><span data-stu-id="791f4-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="791f4-139">لن تطبق عملية التصدير اليدوية التشفير أو نقل الحزمة.</span><span class="sxs-lookup"><span data-stu-id="791f4-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="791f4-140">تكوين بياناتك</span><span class="sxs-lookup"><span data-stu-id="791f4-140">Configure your data</span></span> 

<span data-ttu-id="791f4-141">لمعالجة كشف، يجب عليك تكوين بيانات الموارد البشرية في Talent.</span><span class="sxs-lookup"><span data-stu-id="791f4-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="791f4-142">يجب إعداد بيانات المؤسسة، مثل الوظائف والمناصب، مع معلومات الميزات والتعويضات.</span><span class="sxs-lookup"><span data-stu-id="791f4-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="791f4-143">تتعلق هذه المعلومات بالتوظيف والدفع والخصم وهي معلومات مطلوبة لإنشاء عملية الدفع للموظفين.</span><span class="sxs-lookup"><span data-stu-id="791f4-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="791f4-144">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="791f4-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="791f4-145">ميزات</span><span class="sxs-lookup"><span data-stu-id="791f4-145">Benefits</span></span> 

<span data-ttu-id="791f4-146">توفر الموارد البشرية أدوات يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العاملين التي تقدمها مؤسسة أو تعالجها للعاملين فيها.</span><span class="sxs-lookup"><span data-stu-id="791f4-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="791f4-147">عندما إنشاء ميزات، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="791f4-148">خطط الميزات</span><span class="sxs-lookup"><span data-stu-id="791f4-148">Benefit plans</span></span>

- <span data-ttu-id="791f4-149">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-149">Plan (required)</span></span>
- <span data-ttu-id="791f4-150">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-150">Type (required)</span></span>
- <span data-ttu-id="791f4-151">تأثير كشف المرتبات (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-151">Payroll impact (required)</span></span>
- <span data-ttu-id="791f4-152">استرداد المتأخرات</span><span class="sxs-lookup"><span data-stu-id="791f4-152">Recover arrears</span></span>
- <span data-ttu-id="791f4-153">أسلوب الخصم</span><span class="sxs-lookup"><span data-stu-id="791f4-153">Deduction method</span></span>
- <span data-ttu-id="791f4-154">أولوية الخصم</span><span class="sxs-lookup"><span data-stu-id="791f4-154">Deduction priority</span></span>
- <span data-ttu-id="791f4-155">حد الفترة</span><span class="sxs-lookup"><span data-stu-id="791f4-155">Limit period</span></span>
- <span data-ttu-id="791f4-156">تحديد المبلغ</span><span class="sxs-lookup"><span data-stu-id="791f4-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="791f4-157">ميزات</span><span class="sxs-lookup"><span data-stu-id="791f4-157">Benefits</span></span>

- <span data-ttu-id="791f4-158">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-158">Plan (required)</span></span>
- <span data-ttu-id="791f4-159">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-159">Type (required)</span></span>
- <span data-ttu-id="791f4-160">الخيار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-160">Option (required)</span></span>
- <span data-ttu-id="791f4-161">معرّف الميزة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-161">Benefit ID (required)</span></span>
- <span data-ttu-id="791f4-162">التكرار</span><span class="sxs-lookup"><span data-stu-id="791f4-162">Frequency</span></span>
- <span data-ttu-id="791f4-163">أساس</span><span class="sxs-lookup"><span data-stu-id="791f4-163">Basis</span></span>
- <span data-ttu-id="791f4-164">المبلغ أو النسبة</span><span class="sxs-lookup"><span data-stu-id="791f4-164">Amount or rate</span></span>
- <span data-ttu-id="791f4-165">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="791f4-166">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="791f4-166">Supported frequencies</span></span> 

- <span data-ttu-id="791f4-167">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="791f4-167">Weekly</span></span>
- <span data-ttu-id="791f4-168">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="791f4-168">Bi-weekly</span></span>
- <span data-ttu-id="791f4-169">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="791f4-169">Semi-monthly</span></span>
- <span data-ttu-id="791f4-170">شهري</span><span class="sxs-lookup"><span data-stu-id="791f4-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="791f4-171">الأسس المدعومة</span><span class="sxs-lookup"><span data-stu-id="791f4-171">Supported bases</span></span> 

- <span data-ttu-id="791f4-172">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="791f4-172">Fixed amount</span></span>
- <span data-ttu-id="791f4-173">النسبة المئوية للأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-173">Percent of earnings</span></span>
- <span data-ttu-id="791f4-174">ساعات الإنتاج</span><span class="sxs-lookup"><span data-stu-id="791f4-174">Productive hours</span></span>

<span data-ttu-id="791f4-175">تنشئ خدمة Dayforce الخصومات التالية، استنادًا إلى تأثير كشف المرتبات المحدد في خطة الميزات.</span><span class="sxs-lookup"><span data-stu-id="791f4-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="791f4-176">الاختيار في Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-176">Selection in Talent</span></span>        | <span data-ttu-id="791f4-177">النتيجة في Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="791f4-178">بلا</span><span class="sxs-lookup"><span data-stu-id="791f4-178">None</span></span>                       | <span data-ttu-id="791f4-179">لا يتم إنشاء أي خصم.</span><span class="sxs-lookup"><span data-stu-id="791f4-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="791f4-180">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="791f4-180">Deduction only</span></span>             | <span data-ttu-id="791f4-181">يتم إنشاء خصم الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="791f4-182">المساهمة فقط</span><span class="sxs-lookup"><span data-stu-id="791f4-182">Contribution only</span></span>          | <span data-ttu-id="791f4-183">يتم إنشاء خصم صاحب العمل‬.</span><span class="sxs-lookup"><span data-stu-id="791f4-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="791f4-184">الخصم والمساهمة</span><span class="sxs-lookup"><span data-stu-id="791f4-184">Deduction and contribution</span></span> | <span data-ttu-id="791f4-185">يتم إنشاء خصومات الموظف وصاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="791f4-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="791f4-186">لمزيد من المعلومات حول كيفية تحديد وإدارة برنامج ميزات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="791f4-187">تقديم برنامج ميزات الموظفين</span><span class="sxs-lookup"><span data-stu-id="791f4-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="791f4-188">إنشاء ميزة جديدة</span><span class="sxs-lookup"><span data-stu-id="791f4-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="791f4-189">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="791f4-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="791f4-190">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="791f4-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="791f4-191">التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-191">Compensation</span></span> 

<span data-ttu-id="791f4-192">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="791f4-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="791f4-193">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="791f4-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="791f4-194">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="791f4-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="791f4-195">تستخدم خدمة Dayforce معلومات التعويض لحساب معدل الموظف السنوي أو الساعي.</span><span class="sxs-lookup"><span data-stu-id="791f4-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="791f4-196">وتعتبر خطط التعويض الثابت وتحويلات معدل الدفع مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="791f4-197">يجب ربط الموظفين بخطة تعويض ثابت.</span><span class="sxs-lookup"><span data-stu-id="791f4-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="791f4-198">لمزيد من المعلومات حول خطط التعويض، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="791f4-199">إنشاء خطط التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="791f4-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="791f4-200">إنشاء خطط التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="791f4-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="791f4-201">تطوير خطط وبنية المرتب/التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="791f4-202">تعويض العملية</span><span class="sxs-lookup"><span data-stu-id="791f4-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="791f4-203">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="791f4-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="791f4-204">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="791f4-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="791f4-205">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="791f4-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="791f4-206">الوظائف</span><span class="sxs-lookup"><span data-stu-id="791f4-206">Jobs</span></span> 

<span data-ttu-id="791f4-207">الوظيفة هي مجموعة من المهام والمسؤوليات المطلوبة من الشخص الذي يؤدي وظيفة.</span><span class="sxs-lookup"><span data-stu-id="791f4-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="791f4-208">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="791f4-209">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="791f4-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="791f4-210">تحديد الوظائف الجديدة</span><span class="sxs-lookup"><span data-stu-id="791f4-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="791f4-211">المناصب</span><span class="sxs-lookup"><span data-stu-id="791f4-211">Positions</span></span>

<span data-ttu-id="791f4-212">يعتبر المنصب مثيلاً فرديًا لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="791f4-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="791f4-213">على سبيل المثال، المنصب "مدير المبيعات (شرق)،" هو أحد المناصب المقترنة بالوظيفة، "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="791f4-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="791f4-214">يوجد منصب في قسم.</span><span class="sxs-lookup"><span data-stu-id="791f4-214">A position exists in a department.</span></span> <span data-ttu-id="791f4-215">ويمكن ربط عامل واحد فقط بكل منصب.</span><span class="sxs-lookup"><span data-stu-id="791f4-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="791f4-216">عند إعداد المناصب، يجب أخذ البيانات والتكوينات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="791f4-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="791f4-217">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-217">Position (required)</span></span>
- <span data-ttu-id="791f4-218">الوصف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-218">Description (required)</span></span>
- <span data-ttu-id="791f4-219">الوظيف (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-219">Job (required)</span></span>
- <span data-ttu-id="791f4-220">القسم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-220">Department (required)</span></span>
- <span data-ttu-id="791f4-221">نوع المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-221">Position type (required)</span></span>
- <span data-ttu-id="791f4-222">مكافئ الوقت الكامل</span><span class="sxs-lookup"><span data-stu-id="791f4-222">Full-time equivalent</span></span>
- <span data-ttu-id="791f4-223">الساعات العادية السنوية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="791f4-224">الدفع بواسطة الكيان القانوني (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="791f4-225">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-225">Pay cycle (required)</span></span>
- <span data-ttu-id="791f4-226">البعد المالي الافتراضي – مركز التكلفة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="791f4-227">تعيين العامل – العامل وبدء التعيين وانتهاء التعيين وكود السبب</span><span class="sxs-lookup"><span data-stu-id="791f4-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="791f4-228">عند ارتباط مناصب متعددة في القسم نفسه بالوظيفة نفسها، فسيتم دمجها في منصب واحد في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="791f4-229">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="791f4-230">تنظيم قوة العمل باستخدام الإدارات والوظائف والمناصب</span><span class="sxs-lookup"><span data-stu-id="791f4-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="791f4-231">إعداد المناصب</span><span class="sxs-lookup"><span data-stu-id="791f4-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="791f4-232">الأقسام</span><span class="sxs-lookup"><span data-stu-id="791f4-232">Departments</span></span>

<span data-ttu-id="791f4-233">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="791f4-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="791f4-234">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="791f4-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="791f4-235">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="791f4-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="791f4-236">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="791f4-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="791f4-237">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="791f4-238">إنشاء قسم وإقرانه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="791f4-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="791f4-239">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="791f4-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="791f4-240">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="791f4-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="791f4-241">تحدد دورة الدفع معدل تكرار دفع المرتبات والأيام المحددة التي تُدفع فيها الأجور للعاملين.</span><span class="sxs-lookup"><span data-stu-id="791f4-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="791f4-242">على سبيل المثال، قد تكون دورة الدفع الشهرية وقد تُدفع الأجور للعاملين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="791f4-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="791f4-243">أو، قد تكون دورة الدفع أسبوعية وقد يحصل الموظفون على رواتبهم يوم الثلاثاء بعد انتهاء فترة الدفع.</span><span class="sxs-lookup"><span data-stu-id="791f4-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="791f4-244">يتم تعيين دورات الدفع إلى مناصب للتحكم في الوقت الذي يتم فيه دفع أجور العاملين في هذه المناصب.</span><span class="sxs-lookup"><span data-stu-id="791f4-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="791f4-245">بعد إنشاء دورات الدفع، يمكنك إنشاء فترات دفع لكل دورة.</span><span class="sxs-lookup"><span data-stu-id="791f4-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="791f4-246">تتضمن كل فترة دفع تاريخ دفع افتراضيًا يستند إلى المعلومات التي توفرها.</span><span class="sxs-lookup"><span data-stu-id="791f4-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="791f4-247">ومع ذلك، يمكنك تعديل تاريخ الدفع الافتراضي في فترة دفع للسماح بالاستثناءات، مثل عندما يقع تاريخ الدفع يوم عطلة.</span><span class="sxs-lookup"><span data-stu-id="791f4-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="791f4-248">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="791f4-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="791f4-249">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-249">Pay cycle (required)</span></span>
- <span data-ttu-id="791f4-250">تكرار دورة الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="791f4-251">تاريخ بدء الفترة (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="791f4-252">تاريخ الدفع الافتراضي (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="791f4-253">يتم دمج هذه المعلومات مع Dayforce كمجموعات دفع، ويتم فصلها حسب البلد أو المنطقة لكل دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="791f4-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="791f4-254">يجب إنشاء فترة دفع واحدة على الأقل قبل الدمج.</span><span class="sxs-lookup"><span data-stu-id="791f4-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="791f4-255">تقوم Dayforce بإنشاء تقويمات وتواريخ دفع للمجموعة، استنادًا إلى تاريخ بدء فترة الدفع الأولى وتاريخ الدفع الافتراضي الذي تم تحديده في Talent.</span><span class="sxs-lookup"><span data-stu-id="791f4-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="791f4-256">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-256">Earning codes</span></span>

<span data-ttu-id="791f4-257">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="791f4-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="791f4-258">تحتوي أكواد الأرباح على معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="791f4-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="791f4-259">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="791f4-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="791f4-260">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-260">Earning Code (required)</span></span>
- <span data-ttu-id="791f4-261">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-261">Description</span></span>
- <span data-ttu-id="791f4-262">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="791f4-262">Unit of measure</span></span>
- <span data-ttu-id="791f4-263">منتِج</span><span class="sxs-lookup"><span data-stu-id="791f4-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="791f4-264">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-264">Worker data</span></span>

<span data-ttu-id="791f4-265">تعتبر السجلات الخاصة بمختلف أنواع العاملين مهمة لأنظمة الموارد البشرية وكشوف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="791f4-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="791f4-266">يمكن استخدام المعلومات التي تقوم بإدخالها لتعقب العاملين والمعلومات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="791f4-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="791f4-267">يمكنك المحافظة على المعلومات التالية للعاملين:</span><span class="sxs-lookup"><span data-stu-id="791f4-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="791f4-268">**أساسية** – يمكنك المحافظة على معلومات أساسية حول عامل، مثل معلومات الاتصال والمعلومات الديموغرافية ومعلومات التعريف ومعلومات حول العائلة وحالة الخدمة العسكرية ومعلومات حول المغتربين وجهات الاتصال الشخصية وجهات الاتصال عند الطوارئ.</span><span class="sxs-lookup"><span data-stu-id="791f4-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="791f4-269">**التوظيف** – يمكنك المحافظة على معلومات حول توظيف العامل، مثل معلومات حول شركة أو التبعية لمؤسسة وتعيين المنصب وتاريخي البدء والانتهاء والأهلية للعمل وشروط التوظيف والمعاش والإجازة، وتغيير الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="791f4-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="791f4-270">**الإجازة والغياب** – يمكنك المحافظة على معلومات حول حالات غياب العامل، مثل تقويمات العمل وحركات الغياب وإعداد الغياب.</span><span class="sxs-lookup"><span data-stu-id="791f4-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="791f4-271">**التعويض وكشف المرتبات** – يمكنك المحافظة على معلومات حول خطط تعويض العامل ومعلومات كشف المرتبات، مثل التسجيل في خطة والمكافآت والأداء والعمولة ومعلومات الضريبة والتقاعد والخصومات من الراتب.</span><span class="sxs-lookup"><span data-stu-id="791f4-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="791f4-272">عند إدخال معلومات العامل، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="791f4-273">معلومات عامة</span><span class="sxs-lookup"><span data-stu-id="791f4-273">General information</span></span>

- <span data-ttu-id="791f4-274">رقم الموظف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-274">Personnel number (required)</span></span>
- <span data-ttu-id="791f4-275">الاسم الأول (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-275">First name (required)</span></span>
- <span data-ttu-id="791f4-276">اسم العائلة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-276">Last name (required)</span></span>
- <span data-ttu-id="791f4-277">الاسم الأوسط</span><span class="sxs-lookup"><span data-stu-id="791f4-277">Middle name</span></span>
- <span data-ttu-id="791f4-278">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="791f4-278">Seniority date</span></span>
- <span data-ttu-id="791f4-279">معروف باسم</span><span class="sxs-lookup"><span data-stu-id="791f4-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="791f4-280">معلومات شخصية</span><span class="sxs-lookup"><span data-stu-id="791f4-280">Personal information</span></span>

- <span data-ttu-id="791f4-281">الحالة الاجتماعية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-281">Marital status (required)</span></span>
- <span data-ttu-id="791f4-282">تاريخ الميلاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-282">Birth date (required)</span></span>
- <span data-ttu-id="791f4-283">الجنس (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-283">Gender (required)</span></span>
- <span data-ttu-id="791f4-284">شخص معاق</span><span class="sxs-lookup"><span data-stu-id="791f4-284">Person with disabilities</span></span>
- <span data-ttu-id="791f4-285">منطقة/بلد الجنسية (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="791f4-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="791f4-286">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="791f4-286">Address information</span></span>

- <span data-ttu-id="791f4-287">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-287">Primary (required)</span></span>
- <span data-ttu-id="791f4-288">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-288">Country/region (required)</span></span>
- <span data-ttu-id="791f4-289">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-289">Postal code (required)</span></span>
- <span data-ttu-id="791f4-290">رقم الشارع (مطلوب) (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="791f4-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="791f4-291">ملحق المبنى (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="791f4-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="791f4-292">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-292">City (required)</span></span>
- <span data-ttu-id="791f4-293">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-293">State (required)</span></span>
- <span data-ttu-id="791f4-294">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="791f4-295">معلومات الاتصال</span><span class="sxs-lookup"><span data-stu-id="791f4-295">Contact information</span></span> 

- <span data-ttu-id="791f4-296">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-296">Primary (required)</span></span>
- <span data-ttu-id="791f4-297">رقم الاتصال (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-297">Contact number (required)</span></span>
- <span data-ttu-id="791f4-298">الرقم الداخلي</span><span class="sxs-lookup"><span data-stu-id="791f4-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="791f4-299">معلومات كشف المرتبات وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-299">Payroll information and earning codes</span></span>

<span data-ttu-id="791f4-300">قد يتم تعيين أرباح معينة للموظفين عند معدل تكرار دفع معين، وقد تكون لديهم طريقة دفع مفضلة.</span><span class="sxs-lookup"><span data-stu-id="791f4-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="791f4-301">يتم استخدام الحقول التالية في Dayforce للمساعدة في ضمان استخدام هذه التفضيلات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="791f4-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="791f4-302">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-302">Earning codes</span></span>

- <span data-ttu-id="791f4-303">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-303">Position (required)</span></span>
- <span data-ttu-id="791f4-304">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-304">Earning Code (required)</span></span>
- <span data-ttu-id="791f4-305">التكرار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-305">Frequency (required)</span></span>
- <span data-ttu-id="791f4-306">المبلغ (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="791f4-307">معلومات الراتب</span><span class="sxs-lookup"><span data-stu-id="791f4-307">Payroll information</span></span>

- <span data-ttu-id="791f4-308">طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="791f4-308">Payment Method</span></span>
- <span data-ttu-id="791f4-309">المنطقة الاقتصادية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-309">Economic Region (required)</span></span>
- <span data-ttu-id="791f4-310">معرف ميزات الموظف</span><span class="sxs-lookup"><span data-stu-id="791f4-310">Employee Benefits ID</span></span>
- <span data-ttu-id="791f4-311">رقم المعرف القومي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-311">National ID Number (required)</span></span>
- <span data-ttu-id="791f4-312">رقم الخدمة العسكرية</span><span class="sxs-lookup"><span data-stu-id="791f4-312">Military Service Number</span></span>
- <span data-ttu-id="791f4-313">معرف الوردية (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-313">Shift ID (required)</span></span>
- <span data-ttu-id="791f4-314">رقم الضريبة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-314">Tax Number (required)</span></span>
- <span data-ttu-id="791f4-315">معرّف الاتحاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-315">Union ID (required)</span></span>
- <span data-ttu-id="791f4-316">معرّف يوم العمل (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-316">Work Day ID (required)</span></span>
- <span data-ttu-id="791f4-317">رقم تصريح العمل</span><span class="sxs-lookup"><span data-stu-id="791f4-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="791f4-318">بالنسبة إلى طريقة الدفع، تدعم المكسيك الدفع **نقدًا** وبواسطة **شيك** (الشيك الفعلي للمؤسسة) و**الدفع الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="791f4-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="791f4-319">إذا لم يتم تحديد أي طريقة دفع، فسيتم استخدام **الشيك** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="791f4-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="791f4-320">تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="791f4-320">Employment details</span></span>

<span data-ttu-id="791f4-321">يتم استخدام سجل تفاصيل التوظيف كمعلومات أساسية لاستخراج حالات تعيين موظف وإنهاء خدماته وإعادة تعيينه في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="791f4-322">تدعم خدمة Dayforce سجل توظيف نشط واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="791f4-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="791f4-323">تاريخ بدء التوظيف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-323">Employment start date (required)</span></span>
- <span data-ttu-id="791f4-324">تاريخ انتهاء التوظيف</span><span class="sxs-lookup"><span data-stu-id="791f4-324">Employment end date</span></span>
- <span data-ttu-id="791f4-325">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="791f4-325">Start date</span></span>
- <span data-ttu-id="791f4-326">تاريخ البدء المعدل</span><span class="sxs-lookup"><span data-stu-id="791f4-326">Adjusted start date</span></span>
- <span data-ttu-id="791f4-327">تاريخ إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="791f4-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="791f4-328">سبب إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="791f4-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="791f4-329">يتم استخراج التواريخ الأساسية للموظف باستخدام المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="791f4-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="791f4-330">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-330">Talent</span></span>                | <span data-ttu-id="791f4-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791f4-332">أقرب تاريخ توظيف</span><span class="sxs-lookup"><span data-stu-id="791f4-332">Most recent hire date</span></span> | <span data-ttu-id="791f4-333">تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="791f4-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="791f4-334">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="791f4-334">Termination date</span></span>      | <span data-ttu-id="791f4-335">تاريخ انتهاء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="791f4-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="791f4-336">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="791f4-336">Start date</span></span>            | <span data-ttu-id="791f4-337">تاريخ البدء المعدل أو تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي غير النشط</span><span class="sxs-lookup"><span data-stu-id="791f4-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="791f4-338">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="791f4-338">Original hire date</span></span>    | <span data-ttu-id="791f4-339">تاريخ بدء التوظيف في سجل محفوظات التوظيف الأحدث</span><span class="sxs-lookup"><span data-stu-id="791f4-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="791f4-340">التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-340">Compensation</span></span>

<span data-ttu-id="791f4-341">يجب إقران خطة تعويض ثابت بالمنصب الأساسي لكل موظف خلال فترة التوظيف.</span><span class="sxs-lookup"><span data-stu-id="791f4-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="791f4-342">تبدأ هذه الفترة الزمنية في التاريخ الذي تم تعيين الموظف فيه (أو تاريخ بدء التوظيف) وتستمر حتى إنهاء خدمة الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="791f4-343">تاريخ السريان (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-343">Effective Date (required)</span></span>
- <span data-ttu-id="791f4-344">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="791f4-344">Expiration date</span></span>
- <span data-ttu-id="791f4-345">معدل الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-345">Pay Rate (required)</span></span>
- <span data-ttu-id="791f4-346">تحويلات ‏‫معدل الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="791f4-347">المكافئ السنوي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="791f4-348">المكافئ الساعي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="791f4-349">إذا كان لدى موظف ساعي مناصب متعددة، فسيتم استيراد التعويض الثابت للمنصب الأساسي إلى Dayforce كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="791f4-350">فيما يتعلق بالمناصب غير الأساسية، يُحفظ المعدل الساعي إلى المنصب المناظر في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="791f4-351">إذا كان لدى موظف يتلقى راتبًا مناصب متعددة، فسيتم استخراج المعدل الساعي التراكمي والراتب السنوي عبر كافة المناصب النشطة، وسيتم استخدامها كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="791f4-352">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="791f4-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="791f4-353">معرّف الضمان الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="791f4-353">Social Security identifier</span></span> 

<span data-ttu-id="791f4-354">يجب أن يكون لدى كل موظف معرّفًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="791f4-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="791f4-355">يجب أن يكون هذا المعرّف من نوع التعريف‬ **SSN**.</span><span class="sxs-lookup"><span data-stu-id="791f4-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="791f4-356">في Dayforce، يتم استخراجه تلقائيًا على أنه معرّف الضمان الاجتماعي للموظف المطلوب للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="791f4-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="791f4-357">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-357">Primary (required)</span></span>
- <span data-ttu-id="791f4-358">نوع التعريف = "SSN"</span><span class="sxs-lookup"><span data-stu-id="791f4-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="791f4-359">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="791f4-359">Issued Date</span></span>
- <span data-ttu-id="791f4-360">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="791f4-360">Expiration Date</span></span>

<span data-ttu-id="791f4-361">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **SSN**.</span><span class="sxs-lookup"><span data-stu-id="791f4-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="791f4-362">ومع ذلك، فإن السجل الذي سيتم دمجه في Dayforce هو فقط الذي يحمل العلامة **أساسي**، بصرف النظر عما إذا كان الرقم نشطًا أو منتهي الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="791f4-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="791f4-363">الحسابات البنكية والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="791f4-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="791f4-364">يجب إدخال معلومات صالحة حول الحساب البنكي لأي موظف يختار تلقي الدفع من خلال تحويلات إلى الحساب البنكي‬.</span><span class="sxs-lookup"><span data-stu-id="791f4-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="791f4-365">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-365">Talent</span></span>                         | <span data-ttu-id="791f4-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791f4-367">رقم الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="791f4-368">رمز SWIFT (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-368">SWIFT code (required)</span></span>          | <span data-ttu-id="791f4-369">حقل **معرّف البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="791f4-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="791f4-370">رقم الفرع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="791f4-371">نوع الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-371">Bank account type (required)</span></span>   | <span data-ttu-id="791f4-372">حقل **نوع البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="791f4-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="791f4-373">تتضمن القيم المدعومة **شيكات** و**كشف المرتبات**.</span><span class="sxs-lookup"><span data-stu-id="791f4-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="791f4-374">يتعين على الموظفين الذين اختاروا تلقي الدفع عبر تحويلات إلى الحساب البنكي‬ توفير ارتباط إلى حساب متبقٍ موجود ضمن كيان قانوني عنوانه الأساسي في المكسيك ويقترن بحساب بنكي صالح من بنك مكسيكي.</span><span class="sxs-lookup"><span data-stu-id="791f4-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="791f4-375">يتم تجاهل كافة الحسابات الأخرى غير الحسابات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="791f4-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="791f4-376">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="791f4-376">Address information</span></span>

<span data-ttu-id="791f4-377">يجب أن يكون لدى كل موظف موقعًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="791f4-377">Every employee must have one primary location.</span></span> <span data-ttu-id="791f4-378">في Dayforce، يتم استخدام هذا الموقع لتحديد مكان الإقامة الأساسي للموظف لأغراض ضريبية.</span><span class="sxs-lookup"><span data-stu-id="791f4-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="791f4-379">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-379">Primary (required)</span></span>
- <span data-ttu-id="791f4-380">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-380">Country/region (required)</span></span>
- <span data-ttu-id="791f4-381">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="791f4-382">الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-382">Street (required)</span></span>
- <span data-ttu-id="791f4-383">رقم الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-383">Street Number (required)</span></span>
- <span data-ttu-id="791f4-384">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="791f4-384">Building Complement</span></span>
- <span data-ttu-id="791f4-385">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-385">City (required)</span></span>
- <span data-ttu-id="791f4-386">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-386">State (required)</span></span>
- <span data-ttu-id="791f4-387">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="791f4-388">تكوين البيانات لإنشاء كشف مرتبات في الولايات المتحدة وكندا</span><span class="sxs-lookup"><span data-stu-id="791f4-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="791f4-389">إذا كنت تقوم بإنشاء الدفع للموظفين في الولايات المتحدة وكندا، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="791f4-390">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="791f4-390">Departments are required on positions.</span></span>
- <span data-ttu-id="791f4-391">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="791f4-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="791f4-392">يمكنك تكوين Talent لمطالبة المناصب بتحديد قسم.</span><span class="sxs-lookup"><span data-stu-id="791f4-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="791f4-393">للقيام بذلك، انتقل إلى **الموارد البشرية المناصب المشتركة > المناصب > الأقسام مطلوبة على المناصب**.</span><span class="sxs-lookup"><span data-stu-id="791f4-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="791f4-394">من المستحسن أن يتم فرض هذا الإعداد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="791f4-395">أنواع الوظائف</span><span class="sxs-lookup"><span data-stu-id="791f4-395">Job types</span></span>

<span data-ttu-id="791f4-396">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="791f4-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="791f4-397">تعتبر أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في الولايات المتحدة وكندا.</span><span class="sxs-lookup"><span data-stu-id="791f4-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="791f4-398">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="791f4-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="791f4-399">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="791f4-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="791f4-400">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="791f4-401">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="791f4-401">Job type</span></span>   | <span data-ttu-id="791f4-402">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="791f4-403">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="791f4-403">Hourly</span></span>     | <span data-ttu-id="791f4-404">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="791f4-404">Hourly</span></span>      |
| <span data-ttu-id="791f4-405">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="791f4-405">Salaried</span></span>   | <span data-ttu-id="791f4-406">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="791f4-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="791f4-407">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="791f4-407">Position types</span></span> 

<span data-ttu-id="791f4-408">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="791f4-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="791f4-409">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="791f4-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="791f4-410">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="791f4-411">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="791f4-411">Position type</span></span>   | <span data-ttu-id="791f4-412">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="791f4-413">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="791f4-413">Full-time</span></span>       | <span data-ttu-id="791f4-414">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="791f4-414">Full time employee</span></span> |
| <span data-ttu-id="791f4-415">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="791f4-415">Part-time</span></span>       | <span data-ttu-id="791f4-416">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="791f4-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="791f4-417">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="791f4-417">Reason codes</span></span>

<span data-ttu-id="791f4-418">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="791f4-419">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="791f4-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="791f4-420">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="791f4-421">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="791f4-421">Reason code</span></span>    | <span data-ttu-id="791f4-422">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-422">Description</span></span>      | <span data-ttu-id="791f4-423">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="791f4-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="791f4-424">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="791f4-424">RESIGNATION</span></span>    | <span data-ttu-id="791f4-425">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="791f4-425">Resignation</span></span>      | <span data-ttu-id="791f4-426">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-426">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-427">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="791f4-427">TERMINATION</span></span>    | <span data-ttu-id="791f4-428">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="791f4-428">Termination</span></span>      | <span data-ttu-id="791f4-429">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-429">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-430">التقاعد</span><span class="sxs-lookup"><span data-stu-id="791f4-430">RETIREMENT</span></span>     | <span data-ttu-id="791f4-431">التقاعد</span><span class="sxs-lookup"><span data-stu-id="791f4-431">Retirement</span></span>       | <span data-ttu-id="791f4-432">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-432">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-433">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="791f4-433">OTHER</span></span>          | <span data-ttu-id="791f4-434">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="791f4-434">Other Reasons</span></span>    | <span data-ttu-id="791f4-435">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-435">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-436">الوفاة</span><span class="sxs-lookup"><span data-stu-id="791f4-436">DEATH</span></span>          | <span data-ttu-id="791f4-437">الوفاة</span><span class="sxs-lookup"><span data-stu-id="791f4-437">Death</span></span>            | <span data-ttu-id="791f4-438">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-438">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="791f4-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="791f4-440">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="791f4-440">Leave of Absence</span></span> | <span data-ttu-id="791f4-441">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-441">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="791f4-442">CONTRACTEND</span></span>    | <span data-ttu-id="791f4-443">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="791f4-443">End of Contract</span></span>  | <span data-ttu-id="791f4-444">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-444">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="791f4-445">SALARYCHANGE</span></span>   | <span data-ttu-id="791f4-446">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="791f4-446">Change of Salary</span></span> | <span data-ttu-id="791f4-447">التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="791f4-448">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="791f4-448">Marital status</span></span>

<span data-ttu-id="791f4-449">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="791f4-450">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="791f4-451">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-451">Talent</span></span>                 | <span data-ttu-id="791f4-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="791f4-453">متزوج</span><span class="sxs-lookup"><span data-stu-id="791f4-453">Married</span></span>                | <span data-ttu-id="791f4-454">متزوج</span><span class="sxs-lookup"><span data-stu-id="791f4-454">Married</span></span>              |
| <span data-ttu-id="791f4-455">واحد</span><span class="sxs-lookup"><span data-stu-id="791f4-455">Single</span></span>                 | <span data-ttu-id="791f4-456">واحد</span><span class="sxs-lookup"><span data-stu-id="791f4-456">Single</span></span>               |
| <span data-ttu-id="791f4-457">أرمل</span><span class="sxs-lookup"><span data-stu-id="791f4-457">Widowed</span></span>                | <span data-ttu-id="791f4-458">أرمل</span><span class="sxs-lookup"><span data-stu-id="791f4-458">Widowed</span></span>              |
| <span data-ttu-id="791f4-459">مطلق</span><span class="sxs-lookup"><span data-stu-id="791f4-459">Divorced</span></span>               | <span data-ttu-id="791f4-460">مطلق</span><span class="sxs-lookup"><span data-stu-id="791f4-460">Divorced</span></span>             |
| <span data-ttu-id="791f4-461">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="791f4-461">Registered Partnership</span></span> | <span data-ttu-id="791f4-462">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="791f4-462">Domestic Partnership</span></span> |
| <span data-ttu-id="791f4-463">بلا</span><span class="sxs-lookup"><span data-stu-id="791f4-463">None</span></span>                   | <span data-ttu-id="791f4-464">بلا</span><span class="sxs-lookup"><span data-stu-id="791f4-464">None</span></span>                 |
| <span data-ttu-id="791f4-465">تعايش</span><span class="sxs-lookup"><span data-stu-id="791f4-465">Cohabiting</span></span>             | <span data-ttu-id="791f4-466">تعايش</span><span class="sxs-lookup"><span data-stu-id="791f4-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="791f4-467">الجنس</span><span class="sxs-lookup"><span data-stu-id="791f4-467">Gender</span></span>

<span data-ttu-id="791f4-468">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="791f4-469">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="791f4-470">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-470">Talent</span></span>       | <span data-ttu-id="791f4-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="791f4-472">ذكر</span><span class="sxs-lookup"><span data-stu-id="791f4-472">Male</span></span>         | <span data-ttu-id="791f4-473">ذكر</span><span class="sxs-lookup"><span data-stu-id="791f4-473">Male</span></span>            |
| <span data-ttu-id="791f4-474">أنثى</span><span class="sxs-lookup"><span data-stu-id="791f4-474">Female</span></span>       | <span data-ttu-id="791f4-475">أنثى</span><span class="sxs-lookup"><span data-stu-id="791f4-475">Female</span></span>          |
| <span data-ttu-id="791f4-476">غير محدد</span><span class="sxs-lookup"><span data-stu-id="791f4-476">Non-specific</span></span> | <span data-ttu-id="791f4-477">*غير مدعوم*</span><span class="sxs-lookup"><span data-stu-id="791f4-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="791f4-478">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-478">Earning codes</span></span>

<span data-ttu-id="791f4-479">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="791f4-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="791f4-480">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="791f4-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="791f4-481">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="791f4-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="791f4-482">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="791f4-482">Supported frequencies</span></span>

- <span data-ttu-id="791f4-483">الكل</span><span class="sxs-lookup"><span data-stu-id="791f4-483">All</span></span>
- <span data-ttu-id="791f4-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="791f4-484">EVERYPAY</span></span>
- <span data-ttu-id="791f4-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="791f4-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="791f4-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="791f4-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="791f4-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="791f4-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="791f4-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-488">1OFMTH</span></span>
- <span data-ttu-id="791f4-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-489">LASTOFMTH</span></span>
- <span data-ttu-id="791f4-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-490">2OFMTH</span></span>
- <span data-ttu-id="791f4-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-491">3OFMTH</span></span>
- <span data-ttu-id="791f4-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-492">4OFMTH</span></span>
- <span data-ttu-id="791f4-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-493">5OFMTH</span></span>
- <span data-ttu-id="791f4-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-494">1N2OFMTH</span></span>
- <span data-ttu-id="791f4-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-495">3N4OFMTH</span></span>
- <span data-ttu-id="791f4-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-496">1N3OFMTH</span></span>
- <span data-ttu-id="791f4-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-497">1N4OFMTH</span></span>
- <span data-ttu-id="791f4-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-498">2N3OFMTH</span></span>
- <span data-ttu-id="791f4-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-499">2N4OFMTH</span></span>
- <span data-ttu-id="791f4-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="791f4-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="791f4-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="791f4-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="791f4-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="791f4-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="791f4-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="791f4-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="791f4-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="791f4-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="791f4-512">العناوين</span><span class="sxs-lookup"><span data-stu-id="791f4-512">Addresses</span></span>

<span data-ttu-id="791f4-513">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="791f4-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="791f4-514">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="791f4-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="791f4-515">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-515">Talent</span></span>          | <span data-ttu-id="791f4-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="791f4-517">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="791f4-517">Country/Region</span></span>  | <span data-ttu-id="791f4-518">كود البلد</span><span class="sxs-lookup"><span data-stu-id="791f4-518">Country Code</span></span>          |
| <span data-ttu-id="791f4-519">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="791f4-519">Zip/Postal Code</span></span> | <span data-ttu-id="791f4-520">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="791f4-520">Postal Code</span></span>           |
| <span data-ttu-id="791f4-521">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="791f4-521">State</span></span>           | <span data-ttu-id="791f4-522">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="791f4-522">State Code</span></span>            |
| <span data-ttu-id="791f4-523">المدينة</span><span class="sxs-lookup"><span data-stu-id="791f4-523">City</span></span>            | <span data-ttu-id="791f4-524">المدينة</span><span class="sxs-lookup"><span data-stu-id="791f4-524">City</span></span>                  |
| <span data-ttu-id="791f4-525">الإقليم</span><span class="sxs-lookup"><span data-stu-id="791f4-525">County</span></span>          | <span data-ttu-id="791f4-526">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="791f4-526">County (Municipality)</span></span> |
| <span data-ttu-id="791f4-527">الشارع</span><span class="sxs-lookup"><span data-stu-id="791f4-527">Street</span></span>          | <span data-ttu-id="791f4-528">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="791f4-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="791f4-529">مناطق الضريبة</span><span class="sxs-lookup"><span data-stu-id="791f4-529">Tax regions</span></span>

<span data-ttu-id="791f4-530">تُستخدم مناطق الضريبة لتحديد الضريبة المناسبة التي يجب تطبيقها أثناء إنشاء كشف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="791f4-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="791f4-531">يتم تعيين مناطق الضريبة إلى Dayforce كعناوين موقع.</span><span class="sxs-lookup"><span data-stu-id="791f4-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="791f4-532">يجب أن تكون منطقة الضريبة الافتراضية مقترنة بمنصب العامل النشط.</span><span class="sxs-lookup"><span data-stu-id="791f4-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="791f4-533">منطقة الضريبة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-533">Tax region (required)</span></span>
- <span data-ttu-id="791f4-534">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="791f4-534">Country/Region (required)</span></span>
- <span data-ttu-id="791f4-535">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-535">State (required)</span></span>
- <span data-ttu-id="791f4-536">الإقليم</span><span class="sxs-lookup"><span data-stu-id="791f4-536">County</span></span> 
- <span data-ttu-id="791f4-537">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="791f4-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="791f4-538">تكوين بياناتك لإنشاء كشف المرتبات في المكسيك</span><span class="sxs-lookup"><span data-stu-id="791f4-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="791f4-539">إذا كنت تقوم بإنشاء الدفع للموظفين في المكسيك، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="791f4-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="791f4-540">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="791f4-540">Departments are required on positions.</span></span>
- <span data-ttu-id="791f4-541">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="791f4-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="791f4-542">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="791f4-542">Job types</span></span>

<span data-ttu-id="791f4-543">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="791f4-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="791f4-544">أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="791f4-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="791f4-545">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="791f4-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="791f4-546">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="791f4-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="791f4-547">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="791f4-548">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="791f4-548">Job type</span></span>   | <span data-ttu-id="791f4-549">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="791f4-550">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="791f4-550">Hourly</span></span>     | <span data-ttu-id="791f4-551">الحد الأقصى للأجر في الساعة‬</span><span class="sxs-lookup"><span data-stu-id="791f4-551">MX Hourly</span></span>   |
| <span data-ttu-id="791f4-552">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="791f4-552">Salaried</span></span>   | <span data-ttu-id="791f4-553">الحد الأقصى للراتب</span><span class="sxs-lookup"><span data-stu-id="791f4-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="791f4-554">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="791f4-554">Position types</span></span> 

<span data-ttu-id="791f4-555">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="791f4-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="791f4-556">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="791f4-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="791f4-557">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="791f4-558">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="791f4-558">Position type</span></span>   | <span data-ttu-id="791f4-559">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="791f4-560">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="791f4-560">Full-time</span></span>       | <span data-ttu-id="791f4-561">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="791f4-561">Full time employee</span></span> |
| <span data-ttu-id="791f4-562">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="791f4-562">Part-time</span></span>       | <span data-ttu-id="791f4-563">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="791f4-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="791f4-564">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="791f4-564">Reason codes</span></span>

<span data-ttu-id="791f4-565">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="791f4-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="791f4-566">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="791f4-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="791f4-567">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="791f4-568">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="791f4-568">Reason code</span></span>            | <span data-ttu-id="791f4-569">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-569">Description</span></span>                    | <span data-ttu-id="791f4-570">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="791f4-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="791f4-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="791f4-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="791f4-572">المغادرة قبل كشف المرتبات الأول</span><span class="sxs-lookup"><span data-stu-id="791f4-572">Departure before first payroll</span></span> | <span data-ttu-id="791f4-573">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-573">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-574">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="791f4-574">RESIGNATION</span></span>            | <span data-ttu-id="791f4-575">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="791f4-575">Resignation</span></span>                    | <span data-ttu-id="791f4-576">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-576">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-577">المعاش</span><span class="sxs-lookup"><span data-stu-id="791f4-577">PENSION</span></span>                | <span data-ttu-id="791f4-578">المعاش</span><span class="sxs-lookup"><span data-stu-id="791f4-578">Pension</span></span>                        | <span data-ttu-id="791f4-579">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-579">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-580">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="791f4-580">TERMINATION</span></span>            | <span data-ttu-id="791f4-581">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="791f4-581">Termination</span></span>                    | <span data-ttu-id="791f4-582">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-582">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-583">التقاعد</span><span class="sxs-lookup"><span data-stu-id="791f4-583">RETIREMENT</span></span>             | <span data-ttu-id="791f4-584">التقاعد</span><span class="sxs-lookup"><span data-stu-id="791f4-584">Retirement</span></span>                     | <span data-ttu-id="791f4-585">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-585">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-586">الغائب</span><span class="sxs-lookup"><span data-stu-id="791f4-586">ABSENTEE</span></span>               | <span data-ttu-id="791f4-587">الغائب</span><span class="sxs-lookup"><span data-stu-id="791f4-587">Absentee</span></span>                       | <span data-ttu-id="791f4-588">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-588">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-589">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="791f4-589">OTHER</span></span>                  | <span data-ttu-id="791f4-590">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="791f4-590">Other Reasons</span></span>                  | <span data-ttu-id="791f4-591">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-591">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-592">إقفال</span><span class="sxs-lookup"><span data-stu-id="791f4-592">CLOSURE</span></span>                | <span data-ttu-id="791f4-593">إقفال الشركة</span><span class="sxs-lookup"><span data-stu-id="791f4-593">Business Closure</span></span>               | <span data-ttu-id="791f4-594">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-594">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-595">الوفاة</span><span class="sxs-lookup"><span data-stu-id="791f4-595">DEATH</span></span>                  | <span data-ttu-id="791f4-596">الوفاة</span><span class="sxs-lookup"><span data-stu-id="791f4-596">Death</span></span>                          | <span data-ttu-id="791f4-597">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-597">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="791f4-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="791f4-599">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="791f4-599">Leave of Absence</span></span>               | <span data-ttu-id="791f4-600">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-600">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="791f4-601">CONTRACTEND</span></span>            | <span data-ttu-id="791f4-602">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="791f4-602">End of Contract</span></span>                | <span data-ttu-id="791f4-603">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="791f4-603">Terminate worker</span></span>     |
| <span data-ttu-id="791f4-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="791f4-604">SALARYCHANGE</span></span>           | <span data-ttu-id="791f4-605">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="791f4-605">Change of Salary</span></span>               | <span data-ttu-id="791f4-606">التعويض</span><span class="sxs-lookup"><span data-stu-id="791f4-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="791f4-607">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="791f4-607">Terms of employment</span></span>

<span data-ttu-id="791f4-608">يتم استخدام شروط التوظيف لإنشاء فئات شروط التوظيف.</span><span class="sxs-lookup"><span data-stu-id="791f4-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="791f4-609">يتم تعيين الشروط إلى Dayforce كقيم مؤشر التوظيف.</span><span class="sxs-lookup"><span data-stu-id="791f4-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="791f4-610">شروط التوظيف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="791f4-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="791f4-611">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="791f4-611">Terms of employment</span></span>   | <span data-ttu-id="791f4-612">الوصف</span><span class="sxs-lookup"><span data-stu-id="791f4-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="791f4-613">عادي</span><span class="sxs-lookup"><span data-stu-id="791f4-613">Regular</span></span>               | <span data-ttu-id="791f4-614">عادي</span><span class="sxs-lookup"><span data-stu-id="791f4-614">Regular</span></span>     |
| <span data-ttu-id="791f4-615">مباشر</span><span class="sxs-lookup"><span data-stu-id="791f4-615">Direct</span></span>                | <span data-ttu-id="791f4-616">مباشر</span><span class="sxs-lookup"><span data-stu-id="791f4-616">Direct</span></span>      |
| <span data-ttu-id="791f4-617">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="791f4-617">Internship</span></span>            | <span data-ttu-id="791f4-618">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="791f4-618">Internship</span></span>  |
| <span data-ttu-id="791f4-619">دائم</span><span class="sxs-lookup"><span data-stu-id="791f4-619">Permanent</span></span>             | <span data-ttu-id="791f4-620">دائم</span><span class="sxs-lookup"><span data-stu-id="791f4-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="791f4-621">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="791f4-621">Marital status</span></span>

<span data-ttu-id="791f4-622">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="791f4-623">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="791f4-624">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-624">Talent</span></span>                 | <span data-ttu-id="791f4-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="791f4-626">متزوج</span><span class="sxs-lookup"><span data-stu-id="791f4-626">Married</span></span>                | <span data-ttu-id="791f4-627">متزوج</span><span class="sxs-lookup"><span data-stu-id="791f4-627">Married</span></span>                   |
| <span data-ttu-id="791f4-628">واحد</span><span class="sxs-lookup"><span data-stu-id="791f4-628">Single</span></span>                 | <span data-ttu-id="791f4-629">واحد</span><span class="sxs-lookup"><span data-stu-id="791f4-629">Single</span></span>                    |
| <span data-ttu-id="791f4-630">أرمل</span><span class="sxs-lookup"><span data-stu-id="791f4-630">Widowed</span></span>                | <span data-ttu-id="791f4-631">أرمل</span><span class="sxs-lookup"><span data-stu-id="791f4-631">Widowed</span></span>                   |
| <span data-ttu-id="791f4-632">مطلق</span><span class="sxs-lookup"><span data-stu-id="791f4-632">Divorced</span></span>               | <span data-ttu-id="791f4-633">مطلق</span><span class="sxs-lookup"><span data-stu-id="791f4-633">Divorced</span></span>                  |
| <span data-ttu-id="791f4-634">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="791f4-634">Registered Partnership</span></span> | <span data-ttu-id="791f4-635">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="791f4-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="791f4-636">بلا</span><span class="sxs-lookup"><span data-stu-id="791f4-636">None</span></span>                   | <span data-ttu-id="791f4-637">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="791f4-638">تعايش</span><span class="sxs-lookup"><span data-stu-id="791f4-638">Cohabiting</span></span>             | <span data-ttu-id="791f4-639">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="791f4-640">الجنس</span><span class="sxs-lookup"><span data-stu-id="791f4-640">Gender</span></span>

<span data-ttu-id="791f4-641">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="791f4-642">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="791f4-643">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-643">Talent</span></span>       | <span data-ttu-id="791f4-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="791f4-645">ذكر</span><span class="sxs-lookup"><span data-stu-id="791f4-645">Male</span></span>         | <span data-ttu-id="791f4-646">ذكر</span><span class="sxs-lookup"><span data-stu-id="791f4-646">Male</span></span>                      |
| <span data-ttu-id="791f4-647">أنثى</span><span class="sxs-lookup"><span data-stu-id="791f4-647">Female</span></span>       | <span data-ttu-id="791f4-648">أنثى</span><span class="sxs-lookup"><span data-stu-id="791f4-648">Female</span></span>                    |
| <span data-ttu-id="791f4-649">غير محدد</span><span class="sxs-lookup"><span data-stu-id="791f4-649">Non-specific</span></span> | <span data-ttu-id="791f4-650">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="791f4-651">أسلوب الدفع</span><span class="sxs-lookup"><span data-stu-id="791f4-651">Payment method</span></span>

<span data-ttu-id="791f4-652">تقدم طرق دفع للموظف والشركة طريقة لوصف كيفية تسديد مرتبات وأجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="791f4-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="791f4-653">يتم تعيين طرق الدفع إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="791f4-654">يعرض الجدول التالي كيفية تعيين طرق الدفع إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="791f4-655">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-655">Talent</span></span>             | <span data-ttu-id="791f4-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="791f4-657">نقدي</span><span class="sxs-lookup"><span data-stu-id="791f4-657">Cash</span></span>               | <span data-ttu-id="791f4-658">نقدي</span><span class="sxs-lookup"><span data-stu-id="791f4-658">Cash</span></span>                      |
| <span data-ttu-id="791f4-659">دفع إلكتروني</span><span class="sxs-lookup"><span data-stu-id="791f4-659">Electronic Payment</span></span> | <span data-ttu-id="791f4-660">التحويل</span><span class="sxs-lookup"><span data-stu-id="791f4-660">Transfer</span></span>                  |
| <span data-ttu-id="791f4-661">فحص</span><span class="sxs-lookup"><span data-stu-id="791f4-661">Check</span></span>              | <span data-ttu-id="791f4-662">شيك</span><span class="sxs-lookup"><span data-stu-id="791f4-662">Cheque</span></span>                    |
| <span data-ttu-id="791f4-663">حوالة مصرفية</span><span class="sxs-lookup"><span data-stu-id="791f4-663">Bank Draft</span></span>         | <span data-ttu-id="791f4-664">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="791f4-665">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="791f4-665">Other</span></span>              | <span data-ttu-id="791f4-666">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="791f4-667">نوع الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="791f4-667">Bank account type</span></span>

<span data-ttu-id="791f4-668">يتم استخدام أنواع الحسابات البنكية للدفع الإلكتروني للموظفين.</span><span class="sxs-lookup"><span data-stu-id="791f4-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="791f4-669">يتم تعيين أنواع الحسابات البنكية إلى Dayforce كمعلومات حساب التحويل.</span><span class="sxs-lookup"><span data-stu-id="791f4-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="791f4-670">وتتم ترجمة أنواع الحسابات البنكية، كما هو مناسب، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="791f4-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="791f4-671">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-671">Talent</span></span>            | <span data-ttu-id="791f4-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="791f4-673">حساب شيكات</span><span class="sxs-lookup"><span data-stu-id="791f4-673">Checking Account</span></span>  | <span data-ttu-id="791f4-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="791f4-674">CheckingAccount</span></span>           |
| <span data-ttu-id="791f4-675">حساب الراتب</span><span class="sxs-lookup"><span data-stu-id="791f4-675">Payroll Account</span></span>   | <span data-ttu-id="791f4-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="791f4-676">PayrollAccount</span></span>            |
| <span data-ttu-id="791f4-677">حساب توفير</span><span class="sxs-lookup"><span data-stu-id="791f4-677">Savings Account</span></span>   | <span data-ttu-id="791f4-678">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="791f4-679">حساب BankGirot</span><span class="sxs-lookup"><span data-stu-id="791f4-679">BankGirot account</span></span> | <span data-ttu-id="791f4-680">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="791f4-681">حساب PlusGirot</span><span class="sxs-lookup"><span data-stu-id="791f4-681">PlusGirot account</span></span> | <span data-ttu-id="791f4-682">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="791f4-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="791f4-683">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="791f4-683">Earning codes</span></span>

<span data-ttu-id="791f4-684">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="791f4-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="791f4-685">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="791f4-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="791f4-686">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="791f4-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="791f4-687">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="791f4-687">Supported frequencies</span></span>

- <span data-ttu-id="791f4-688">الكل</span><span class="sxs-lookup"><span data-stu-id="791f4-688">All</span></span>
- <span data-ttu-id="791f4-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="791f4-689">EVERYPAY</span></span>
- <span data-ttu-id="791f4-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="791f4-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="791f4-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="791f4-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="791f4-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="791f4-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="791f4-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-693">1OFMTH</span></span>
- <span data-ttu-id="791f4-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-694">LASTOFMTH</span></span>
- <span data-ttu-id="791f4-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-695">2OFMTH</span></span>
- <span data-ttu-id="791f4-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-696">3OFMTH</span></span>
- <span data-ttu-id="791f4-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-697">4OFMTH</span></span>
- <span data-ttu-id="791f4-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-698">5OFMTH</span></span>
- <span data-ttu-id="791f4-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-699">1N2OFMTH</span></span>
- <span data-ttu-id="791f4-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-700">3N4OFMTH</span></span>
- <span data-ttu-id="791f4-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-701">1N3OFMTH</span></span>
- <span data-ttu-id="791f4-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-702">1N4OFMTH</span></span>
- <span data-ttu-id="791f4-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-703">2N3OFMTH</span></span>
- <span data-ttu-id="791f4-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-704">2N4OFMTH</span></span>
- <span data-ttu-id="791f4-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="791f4-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="791f4-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="791f4-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="791f4-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="791f4-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="791f4-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="791f4-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="791f4-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="791f4-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="791f4-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="791f4-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="791f4-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="791f4-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="791f4-717">العناوين</span><span class="sxs-lookup"><span data-stu-id="791f4-717">Addresses</span></span>

<span data-ttu-id="791f4-718">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="791f4-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="791f4-719">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="791f4-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="791f4-720">Talent</span><span class="sxs-lookup"><span data-stu-id="791f4-720">Talent</span></span>              | <span data-ttu-id="791f4-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="791f4-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="791f4-722">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="791f4-722">Country/Region</span></span>      | <span data-ttu-id="791f4-723">كود البلد</span><span class="sxs-lookup"><span data-stu-id="791f4-723">Country Code</span></span>          |
| <span data-ttu-id="791f4-724">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="791f4-724">Zip/Postal Code</span></span>     | <span data-ttu-id="791f4-725">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="791f4-725">Postal Code</span></span>           |
| <span data-ttu-id="791f4-726">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="791f4-726">State</span></span>               | <span data-ttu-id="791f4-727">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="791f4-727">State Code</span></span>            |
| <span data-ttu-id="791f4-728">المدينة</span><span class="sxs-lookup"><span data-stu-id="791f4-728">City</span></span>                | <span data-ttu-id="791f4-729">المدينة</span><span class="sxs-lookup"><span data-stu-id="791f4-729">City</span></span>                  |
| <span data-ttu-id="791f4-730">الإقليم</span><span class="sxs-lookup"><span data-stu-id="791f4-730">County</span></span>              | <span data-ttu-id="791f4-731">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="791f4-731">County (Municipality)</span></span> |
| <span data-ttu-id="791f4-732">الشارع</span><span class="sxs-lookup"><span data-stu-id="791f4-732">Street</span></span>              | <span data-ttu-id="791f4-733">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="791f4-733">Address Line 1</span></span>        |
| <span data-ttu-id="791f4-734">رقم الشارع</span><span class="sxs-lookup"><span data-stu-id="791f4-734">Street Number</span></span>       | <span data-ttu-id="791f4-735">سطر العنوان 2</span><span class="sxs-lookup"><span data-stu-id="791f4-735">Address Line 2</span></span>        |
| <span data-ttu-id="791f4-736">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="791f4-736">Building Complement</span></span> | <span data-ttu-id="791f4-737">سطر العنوان 5</span><span class="sxs-lookup"><span data-stu-id="791f4-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="791f4-738">رقم جواز السفر</span><span class="sxs-lookup"><span data-stu-id="791f4-738">Passport number</span></span>

<span data-ttu-id="791f4-739">بإمكان الموظفين إعلان معلومات جواز السفر.</span><span class="sxs-lookup"><span data-stu-id="791f4-739">Employees can declare passport information.</span></span> <span data-ttu-id="791f4-740">هذه المعلومات هي نوع من أنواع تعريف **جواز السفر** وهي تتكامل في Dayforce كجزء من معلومات الموظف خاصة بالمكسيك.</span><span class="sxs-lookup"><span data-stu-id="791f4-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="791f4-741">نوع التعريف = "جواز سفر"</span><span class="sxs-lookup"><span data-stu-id="791f4-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="791f4-742">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="791f4-742">Issued Date</span></span>
- <span data-ttu-id="791f4-743">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="791f4-743">Expiration Date</span></span>

<span data-ttu-id="791f4-744">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **جواز سفر**.</span><span class="sxs-lookup"><span data-stu-id="791f4-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="791f4-745">ومع ذلك، يتم دمج إدخال جواز السفر النشط الحالي فقط في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="791f4-746">إذا انتهت صلاحية جميع إدخالات جوازات السفر، فسيتكامل جواز السفر الذي تم إصداره مؤخرًا في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="791f4-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
