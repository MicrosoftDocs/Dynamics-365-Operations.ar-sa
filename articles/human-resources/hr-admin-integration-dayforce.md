---
title: 'تكوين التكامل مع Dayforce '
description: يعتمد التكامل بين Microsoft Dynamics 365 Human Resources وCeridian Dayforce على العديد من خطوات التكوين الموضحة في هذا المقال. يجب عليك تكوين التكامل في كل من Human Resources وDayforce قبل أن تتمكن من معالجة دورة دفع.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85e7274b0e9c130e5c3426fd1fff98410f93e49a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007914"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="392fd-104">تكوين التكامل مع Dayforce </span><span class="sxs-lookup"><span data-stu-id="392fd-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="392fd-105">يعتمد التكامل بين Microsoft Dynamics 365 Human Resources وCeridian Dayforce على العديد من خطوات التكوين الموضحة في هذا المقال.</span><span class="sxs-lookup"><span data-stu-id="392fd-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="392fd-106">يجب عليك تكوين التكامل في كل من Human Resources وDayforce قبل أن تتمكن من معالجة دورة دفع.</span><span class="sxs-lookup"><span data-stu-id="392fd-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="392fd-107">عندما تستخدم خدمة مثل Dayforce لإتمام دورات الدفع، يجب عليك تمكين التكامل في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="392fd-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="392fd-108">يتطلب التكامل بيانات معينة من Human Resources.</span><span class="sxs-lookup"><span data-stu-id="392fd-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="392fd-109">لذلك، يجب عليك التأكد من أن البيانات التي تم تعيينها إلى Dayforce هي بيانات تم تكوينها في Human Resources بطريقة تدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="392fd-110">يستخدم التكامل الفئات الواسعة التالية من البيانات:</span><span class="sxs-lookup"><span data-stu-id="392fd-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="392fd-111">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-111">Human resources data</span></span>
- <span data-ttu-id="392fd-112">بيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-112">Compensation data</span></span>
- <span data-ttu-id="392fd-113">بيانات كشف المرتبات، مثل دورات الدفع وفترات الدفع وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="392fd-114">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-114">Worker data</span></span>

<span data-ttu-id="392fd-115">يصف هذا المقال الخطوات التي يجب اتباعها لتمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="392fd-116">ويشرح أيضًا أنواع البيانات وتفاصيل التكوين التي يحتاج إليها التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="392fd-117">تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="392fd-117">Enable the integration</span></span>

<span data-ttu-id="392fd-118">في Human Resources، يجب تشغيل التكامل وإدخال معلومات التكوين للاتصال بخدمة Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="392fd-119">إذا أردت أن يتم استيراد حركة دفتر الأستاذ العام التي نشأت إلى Microsoft Dynamics 365 Finance، فيجب أيضًا إعداد حساب تخزين في Microsoft Azure وإدخال سلسلة اتصال Azure Storage في Finance.</span><span class="sxs-lookup"><span data-stu-id="392fd-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="392fd-120">لتشغيل التكامل في Human Resources، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="392fd-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="392fd-121">في صفحة **إدارة النظام**، حدد **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="392fd-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="392fd-122">أدخل نقطة نهاية بروتوكول نقل الملفات (FTP) الآمنة ومسار مجلد FTP الآمن.</span><span class="sxs-lookup"><span data-stu-id="392fd-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="392fd-123">أدخل اسم المستخدم وكلمة المرور للمستخدم الذي سينتقل إلى نقطة النهاية الآمنة ومسار المجلد الآمن في بروتوكول FTP.</span><span class="sxs-lookup"><span data-stu-id="392fd-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="392fd-124">اختبر الاتصال، كما تقتضي الحاجة، وعيّن الخيار **تمكين تكامل كشف المرتبات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="392fd-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="392fd-125">عند تشغيل التكامل، يتم إنشاء حزمة وملفات تصدير البيانات ويتم تعيين معدل التكرار.</span><span class="sxs-lookup"><span data-stu-id="392fd-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="392fd-126">ويمكنك تغيير معدل التكرار وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="392fd-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="392fd-127">لمزيد من المعلومات حول حسابات مساحة تخزين Azure وسلاسل اتصال مساحة تخزين Azure، راجع مقالات Azure التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="392fd-128">حول حسابات مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="392fd-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="392fd-129">تكوين سلاسل اتصال مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="392fd-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="392fd-130">تفاصيل تقنية عند تمكين تكامل الرواتب</span><span class="sxs-lookup"><span data-stu-id="392fd-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="392fd-131">يؤدي تشغيل تكامل الرواتب إلى تأثيرين أساسيين:</span><span class="sxs-lookup"><span data-stu-id="392fd-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="392fd-132">يتم إنشاء مشروع تصدير بيانات يُسمى "تصدير تكامل الرواتب".</span><span class="sxs-lookup"><span data-stu-id="392fd-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="392fd-133">يحتوي هذا المشروع على الكيانات والحقول المطلوبة لتكامل الرواتب.</span><span class="sxs-lookup"><span data-stu-id="392fd-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="392fd-134">لفحص المشروع، انتقل إلى **إدارة النظام**، وحدد تجانب**إدارة البيانات**، ثم افتح مشروع البيانات من قائمة المشروعات.</span><span class="sxs-lookup"><span data-stu-id="392fd-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="392fd-135">تنفذ هذه الوظيفة الدفعية مشروع تصدير البيانات، وتشفر حزمة البيانات الناتجة، وتنقل ملف حزمة البيانات إلى نقطة نهاية SFTP التي تم تكوينها على شاشة **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="392fd-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="392fd-136">يتم تشفير حزمة البيانات التي تم نقلها إلى نقطة نهاية SFTP باستخدام مفتاح فريد للحزمة.</span><span class="sxs-lookup"><span data-stu-id="392fd-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="392fd-137">المفتاح موجود في Azure Key Vault والذي يمكن الوصول إليه عن طريق Ceridian فقط.</span><span class="sxs-lookup"><span data-stu-id="392fd-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="392fd-138">لا يمكن فك تشفير محتويات حزمة البيانات وفحصها.</span><span class="sxs-lookup"><span data-stu-id="392fd-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="392fd-139">إذا كنت بحاجة إلى فحص محتويات حزمة البيانات، ستحتاج إلى تصدير مشروع البيانات "تصدير تكامل الرواتب" يدويا، وتنزيله، ثم فتحه.</span><span class="sxs-lookup"><span data-stu-id="392fd-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="392fd-140">لن تطبق عملية التصدير اليدوية التشفير أو نقل الحزمة.</span><span class="sxs-lookup"><span data-stu-id="392fd-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="392fd-141">تكوين بياناتك</span><span class="sxs-lookup"><span data-stu-id="392fd-141">Configure your data</span></span> 

<span data-ttu-id="392fd-142">لمعالجة كشف، يجب عليك تكوين بيانات Human Resources في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="392fd-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="392fd-143">يجب إعداد بيانات المؤسسة، مثل الوظائف والمناصب، مع معلومات الميزات والتعويضات.</span><span class="sxs-lookup"><span data-stu-id="392fd-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="392fd-144">تتعلق هذه المعلومات بالتوظيف والدفع والخصم وهي معلومات مطلوبة لإنشاء عملية الدفع للموظفين.</span><span class="sxs-lookup"><span data-stu-id="392fd-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="392fd-145">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="392fd-146">ميزات</span><span class="sxs-lookup"><span data-stu-id="392fd-146">Benefits</span></span> 

<span data-ttu-id="392fd-147">توفر الموارد البشرية أدوات يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العاملين التي تقدمها مؤسسة أو تعالجها للعاملين فيها.</span><span class="sxs-lookup"><span data-stu-id="392fd-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="392fd-148">عندما إنشاء ميزات، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="392fd-149">خطط الميزات</span><span class="sxs-lookup"><span data-stu-id="392fd-149">Benefit plans</span></span>

- <span data-ttu-id="392fd-150">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-150">Plan (required)</span></span>
- <span data-ttu-id="392fd-151">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-151">Type (required)</span></span>
- <span data-ttu-id="392fd-152">تأثير كشف المرتبات (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-152">Payroll impact (required)</span></span>
- <span data-ttu-id="392fd-153">استرداد المتأخرات</span><span class="sxs-lookup"><span data-stu-id="392fd-153">Recover arrears</span></span>
- <span data-ttu-id="392fd-154">أسلوب الخصم</span><span class="sxs-lookup"><span data-stu-id="392fd-154">Deduction method</span></span>
- <span data-ttu-id="392fd-155">أولوية الخصم</span><span class="sxs-lookup"><span data-stu-id="392fd-155">Deduction priority</span></span>
- <span data-ttu-id="392fd-156">حد الفترة</span><span class="sxs-lookup"><span data-stu-id="392fd-156">Limit period</span></span>
- <span data-ttu-id="392fd-157">تحديد المبلغ</span><span class="sxs-lookup"><span data-stu-id="392fd-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="392fd-158">ميزات</span><span class="sxs-lookup"><span data-stu-id="392fd-158">Benefits</span></span>

- <span data-ttu-id="392fd-159">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-159">Plan (required)</span></span>
- <span data-ttu-id="392fd-160">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-160">Type (required)</span></span>
- <span data-ttu-id="392fd-161">الخيار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-161">Option (required)</span></span>
- <span data-ttu-id="392fd-162">معرّف الميزة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-162">Benefit ID (required)</span></span>
- <span data-ttu-id="392fd-163">التكرار</span><span class="sxs-lookup"><span data-stu-id="392fd-163">Frequency</span></span>
- <span data-ttu-id="392fd-164">أساس</span><span class="sxs-lookup"><span data-stu-id="392fd-164">Basis</span></span>
- <span data-ttu-id="392fd-165">المبلغ أو النسبة</span><span class="sxs-lookup"><span data-stu-id="392fd-165">Amount or rate</span></span>
- <span data-ttu-id="392fd-166">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="392fd-167">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="392fd-167">Supported frequencies</span></span> 

- <span data-ttu-id="392fd-168">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="392fd-168">Weekly</span></span>
- <span data-ttu-id="392fd-169">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="392fd-169">Bi-weekly</span></span>
- <span data-ttu-id="392fd-170">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="392fd-170">Semi-monthly</span></span>
- <span data-ttu-id="392fd-171">شهري</span><span class="sxs-lookup"><span data-stu-id="392fd-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="392fd-172">الأسس المدعومة</span><span class="sxs-lookup"><span data-stu-id="392fd-172">Supported bases</span></span> 

- <span data-ttu-id="392fd-173">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="392fd-173">Fixed amount</span></span>
- <span data-ttu-id="392fd-174">النسبة المئوية للأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-174">Percent of earnings</span></span>
- <span data-ttu-id="392fd-175">ساعات الإنتاج</span><span class="sxs-lookup"><span data-stu-id="392fd-175">Productive hours</span></span>

<span data-ttu-id="392fd-176">تنشئ خدمة Dayforce الخصومات التالية، استنادًا إلى تأثير كشف المرتبات المحدد في خطة الميزات.</span><span class="sxs-lookup"><span data-stu-id="392fd-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="392fd-177">التحديد في Human Resources</span><span class="sxs-lookup"><span data-stu-id="392fd-177">Selection in Human Resources</span></span>        | <span data-ttu-id="392fd-178">النتيجة في Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="392fd-179">لا‬‬ شيء</span><span class="sxs-lookup"><span data-stu-id="392fd-179">None</span></span>                       | <span data-ttu-id="392fd-180">لا يتم إنشاء أي خصم.</span><span class="sxs-lookup"><span data-stu-id="392fd-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="392fd-181">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="392fd-181">Deduction only</span></span>             | <span data-ttu-id="392fd-182">يتم إنشاء خصم الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="392fd-183">المساهمة فقط</span><span class="sxs-lookup"><span data-stu-id="392fd-183">Contribution only</span></span>          | <span data-ttu-id="392fd-184">يتم إنشاء خصم صاحب العمل‬.</span><span class="sxs-lookup"><span data-stu-id="392fd-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="392fd-185">الخصم والمساهمة</span><span class="sxs-lookup"><span data-stu-id="392fd-185">Deduction and contribution</span></span> | <span data-ttu-id="392fd-186">يتم إنشاء خصومات الموظف وصاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="392fd-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="392fd-187">لمزيد من المعلومات حول كيفية تحديد وإدارة برنامج ميزات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="392fd-188">تقديم برنامج ميزات الموظفين</span><span class="sxs-lookup"><span data-stu-id="392fd-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="392fd-189">إنشاء ميزة جديدة</span><span class="sxs-lookup"><span data-stu-id="392fd-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="392fd-190">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="392fd-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="392fd-191">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="392fd-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="392fd-192">التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-192">Compensation</span></span> 

<span data-ttu-id="392fd-193">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="392fd-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="392fd-194">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="392fd-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="392fd-195">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="392fd-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="392fd-196">تستخدم خدمة Dayforce معلومات التعويض لحساب معدل الموظف السنوي أو الساعي.</span><span class="sxs-lookup"><span data-stu-id="392fd-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="392fd-197">وتعتبر خطط التعويض الثابت وتحويلات معدل الدفع مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="392fd-198">يجب ربط الموظفين بخطة تعويض ثابت.</span><span class="sxs-lookup"><span data-stu-id="392fd-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="392fd-199">لمزيد من المعلومات حول خطط التعويض، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="392fd-200">إنشاء خطط التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="392fd-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="392fd-201">إنشاء خطط التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="392fd-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="392fd-202">تطوير خطط وبنية المرتب/التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="392fd-203">تعويض العملية</span><span class="sxs-lookup"><span data-stu-id="392fd-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="392fd-204">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="392fd-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="392fd-205">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="392fd-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="392fd-206">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="392fd-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="392fd-207">الوظائف</span><span class="sxs-lookup"><span data-stu-id="392fd-207">Jobs</span></span> 

<span data-ttu-id="392fd-208">الوظيفة هي مجموعة من المهام والمسؤوليات المطلوبة من الشخص الذي يؤدي وظيفة.</span><span class="sxs-lookup"><span data-stu-id="392fd-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="392fd-209">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="392fd-210">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="392fd-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="392fd-211">تحديد الوظائف الجديدة</span><span class="sxs-lookup"><span data-stu-id="392fd-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="392fd-212">المناصب‬</span><span class="sxs-lookup"><span data-stu-id="392fd-212">Positions</span></span>

<span data-ttu-id="392fd-213">يعتبر المنصب مثيلاً فرديًا لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="392fd-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="392fd-214">على سبيل المثال، المنصب "مدير المبيعات (شرق)،" هو أحد المناصب المقترنة بالوظيفة، "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="392fd-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="392fd-215">يوجد منصب في قسم.</span><span class="sxs-lookup"><span data-stu-id="392fd-215">A position exists in a department.</span></span> <span data-ttu-id="392fd-216">ويمكن ربط عامل واحد فقط بكل منصب.</span><span class="sxs-lookup"><span data-stu-id="392fd-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="392fd-217">عند إعداد المناصب، يجب أخذ البيانات والتكوينات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="392fd-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="392fd-218">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-218">Position (required)</span></span>
- <span data-ttu-id="392fd-219">الوصف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-219">Description (required)</span></span>
- <span data-ttu-id="392fd-220">الوظيف (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-220">Job (required)</span></span>
- <span data-ttu-id="392fd-221">القسم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-221">Department (required)</span></span>
- <span data-ttu-id="392fd-222">نوع المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-222">Position type (required)</span></span>
- <span data-ttu-id="392fd-223">مكافئ الوقت الكامل</span><span class="sxs-lookup"><span data-stu-id="392fd-223">Full-time equivalent</span></span>
- <span data-ttu-id="392fd-224">الساعات العادية السنوية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="392fd-225">الدفع بواسطة الكيان القانوني (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="392fd-226">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-226">Pay cycle (required)</span></span>
- <span data-ttu-id="392fd-227">البعد المالي الافتراضي – مركز التكلفة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="392fd-228">تعيين العامل – العامل وبدء التعيين وانتهاء التعيين وكود السبب</span><span class="sxs-lookup"><span data-stu-id="392fd-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="392fd-229">عند ارتباط مناصب متعددة في القسم نفسه بالوظيفة نفسها، فسيتم دمجها في منصب واحد في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="392fd-230">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="392fd-231">تنظيم القوى العاملة باستخدام الإدارات والوظائف والمناصب</span><span class="sxs-lookup"><span data-stu-id="392fd-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="392fd-232">إعداد المناصب</span><span class="sxs-lookup"><span data-stu-id="392fd-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="392fd-233">الأقسام</span><span class="sxs-lookup"><span data-stu-id="392fd-233">Departments</span></span>

<span data-ttu-id="392fd-234">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="392fd-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="392fd-235">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="392fd-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="392fd-236">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="392fd-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="392fd-237">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="392fd-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="392fd-238">لمزيد من المعلومات، راجع المقالات التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="392fd-239">إنشاء قسم وإقرانه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="392fd-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="392fd-240">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="392fd-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="392fd-241">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="392fd-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="392fd-242">تحدد دورة الدفع معدل تكرار دفع المرتبات والأيام المحددة التي تُدفع فيها الأجور للعاملين.</span><span class="sxs-lookup"><span data-stu-id="392fd-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="392fd-243">على سبيل المثال، قد تكون دورة الدفع الشهرية وقد تُدفع الأجور للعاملين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="392fd-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="392fd-244">أو، قد تكون دورة الدفع أسبوعية وقد يحصل الموظفون على رواتبهم يوم الثلاثاء بعد انتهاء فترة الدفع.</span><span class="sxs-lookup"><span data-stu-id="392fd-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="392fd-245">يتم تعيين دورات الدفع إلى مناصب للتحكم في الوقت الذي يتم فيه دفع أجور العاملين في هذه المناصب.</span><span class="sxs-lookup"><span data-stu-id="392fd-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="392fd-246">بعد إنشاء دورات الدفع، يمكنك إنشاء فترات دفع لكل دورة.</span><span class="sxs-lookup"><span data-stu-id="392fd-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="392fd-247">تتضمن كل فترة دفع تاريخ دفع افتراضيًا يستند إلى المعلومات التي توفرها.</span><span class="sxs-lookup"><span data-stu-id="392fd-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="392fd-248">ومع ذلك، يمكنك تعديل تاريخ الدفع الافتراضي في فترة دفع للسماح بالاستثناءات، مثل عندما يقع تاريخ الدفع يوم عطلة.</span><span class="sxs-lookup"><span data-stu-id="392fd-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="392fd-249">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="392fd-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="392fd-250">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-250">Pay cycle (required)</span></span>
- <span data-ttu-id="392fd-251">تكرار دورة الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="392fd-252">تاريخ بدء الفترة (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="392fd-253">تاريخ الدفع الافتراضي (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="392fd-254">يتم دمج هذه المعلومات مع Dayforce كمجموعات دفع، ويتم فصلها حسب البلد أو المنطقة لكل دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="392fd-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="392fd-255">يجب إنشاء فترة دفع واحدة على الأقل قبل الدمج.</span><span class="sxs-lookup"><span data-stu-id="392fd-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="392fd-256">تقوم Dayforce بإنشاء تقويمات وتواريخ دفع للمجموعة، استنادًا إلى تاريخ بدء فترة الدفع الأولى وتاريخ الدفع الافتراضي الذي تم تحديده في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="392fd-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="392fd-257">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-257">Earning codes</span></span>

<span data-ttu-id="392fd-258">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="392fd-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="392fd-259">تحتوي أكواد الأرباح على معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="392fd-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="392fd-260">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="392fd-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="392fd-261">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-261">Earning Code (required)</span></span>
- <span data-ttu-id="392fd-262">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-262">Description</span></span>
- <span data-ttu-id="392fd-263">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="392fd-263">Unit of measure</span></span>
- <span data-ttu-id="392fd-264">منتِج</span><span class="sxs-lookup"><span data-stu-id="392fd-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="392fd-265">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-265">Worker data</span></span>

<span data-ttu-id="392fd-266">تعتبر السجلات الخاصة بمختلف أنواع العاملين مهمة لأنظمة الموارد البشرية وكشوف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="392fd-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="392fd-267">يمكن استخدام المعلومات التي تقوم بإدخالها لتعقب العاملين والمعلومات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="392fd-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="392fd-268">يمكنك المحافظة على المعلومات التالية للعاملين:</span><span class="sxs-lookup"><span data-stu-id="392fd-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="392fd-269">**أساسية** – يمكنك المحافظة على معلومات أساسية حول عامل، مثل معلومات الاتصال والمعلومات الديموغرافية ومعلومات التعريف ومعلومات حول العائلة وحالة الخدمة العسكرية ومعلومات حول المغتربين وجهات الاتصال الشخصية وجهات الاتصال عند الطوارئ.</span><span class="sxs-lookup"><span data-stu-id="392fd-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="392fd-270">**التوظيف** – يمكنك المحافظة على معلومات حول توظيف العامل، مثل معلومات حول شركة أو التبعية لمؤسسة وتعيين المنصب وتاريخي البدء والانتهاء والأهلية للعمل وشروط التوظيف والمعاش والإجازة، وتغيير الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="392fd-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="392fd-271">**الإجازة والغياب** – يمكنك المحافظة على معلومات حول حالات غياب العامل، مثل تقويمات العمل وحركات الغياب وإعداد الغياب.</span><span class="sxs-lookup"><span data-stu-id="392fd-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="392fd-272">**التعويض وكشف المرتبات** – يمكنك المحافظة على معلومات حول خطط تعويض العامل ومعلومات كشف المرتبات، مثل التسجيل في خطة والمكافآت والأداء والعمولة ومعلومات الضريبة والتقاعد والخصومات من الراتب.</span><span class="sxs-lookup"><span data-stu-id="392fd-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="392fd-273">عند إدخال معلومات العامل، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="392fd-274">معلومات عامة</span><span class="sxs-lookup"><span data-stu-id="392fd-274">General information</span></span>

- <span data-ttu-id="392fd-275">رقم الموظف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-275">Personnel number (required)</span></span>
- <span data-ttu-id="392fd-276">الاسم الأول (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-276">First name (required)</span></span>
- <span data-ttu-id="392fd-277">اسم العائلة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-277">Last name (required)</span></span>
- <span data-ttu-id="392fd-278">الاسم الأوسط</span><span class="sxs-lookup"><span data-stu-id="392fd-278">Middle name</span></span>
- <span data-ttu-id="392fd-279">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="392fd-279">Seniority date</span></span>
- <span data-ttu-id="392fd-280">معروف باسم</span><span class="sxs-lookup"><span data-stu-id="392fd-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="392fd-281">معلومات شخصية</span><span class="sxs-lookup"><span data-stu-id="392fd-281">Personal information</span></span>

- <span data-ttu-id="392fd-282">الحالة الاجتماعية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-282">Marital status (required)</span></span>
- <span data-ttu-id="392fd-283">تاريخ الميلاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-283">Birth date (required)</span></span>
- <span data-ttu-id="392fd-284">الجنس (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-284">Gender (required)</span></span>
- <span data-ttu-id="392fd-285">شخص معاق</span><span class="sxs-lookup"><span data-stu-id="392fd-285">Person with disabilities</span></span>
- <span data-ttu-id="392fd-286">منطقة/بلد الجنسية (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="392fd-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="392fd-287">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="392fd-287">Address information</span></span>

- <span data-ttu-id="392fd-288">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-288">Primary (required)</span></span>
- <span data-ttu-id="392fd-289">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-289">Country/region (required)</span></span>
- <span data-ttu-id="392fd-290">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-290">Postal code (required)</span></span>
- <span data-ttu-id="392fd-291">رقم الشارع (مطلوب) (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="392fd-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="392fd-292">ملحق المبنى (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="392fd-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="392fd-293">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-293">City (required)</span></span>
- <span data-ttu-id="392fd-294">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-294">State (required)</span></span>
- <span data-ttu-id="392fd-295">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="392fd-296">معلومات الاتصال</span><span class="sxs-lookup"><span data-stu-id="392fd-296">Contact information</span></span> 

- <span data-ttu-id="392fd-297">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-297">Primary (required)</span></span>
- <span data-ttu-id="392fd-298">رقم الاتصال (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-298">Contact number (required)</span></span>
- <span data-ttu-id="392fd-299">الرقم الداخلي</span><span class="sxs-lookup"><span data-stu-id="392fd-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="392fd-300">معلومات كشف المرتبات وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-300">Payroll information and earning codes</span></span>

<span data-ttu-id="392fd-301">قد يتم تعيين أرباح معينة للموظفين عند معدل تكرار دفع معين، وقد تكون لديهم طريقة دفع مفضلة.</span><span class="sxs-lookup"><span data-stu-id="392fd-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="392fd-302">يتم استخدام الحقول التالية في Dayforce للمساعدة في ضمان استخدام هذه التفضيلات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="392fd-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="392fd-303">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-303">Earning codes</span></span>

- <span data-ttu-id="392fd-304">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-304">Position (required)</span></span>
- <span data-ttu-id="392fd-305">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-305">Earning Code (required)</span></span>
- <span data-ttu-id="392fd-306">التكرار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-306">Frequency (required)</span></span>
- <span data-ttu-id="392fd-307">المبلغ (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="392fd-308">معلومات الراتب</span><span class="sxs-lookup"><span data-stu-id="392fd-308">Payroll information</span></span>

- <span data-ttu-id="392fd-309">طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="392fd-309">Payment Method</span></span>
- <span data-ttu-id="392fd-310">المنطقة الاقتصادية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-310">Economic Region (required)</span></span>
- <span data-ttu-id="392fd-311">معرف ميزات الموظف</span><span class="sxs-lookup"><span data-stu-id="392fd-311">Employee Benefits ID</span></span>
- <span data-ttu-id="392fd-312">رقم المعرف القومي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-312">National ID Number (required)</span></span>
- <span data-ttu-id="392fd-313">رقم الخدمة العسكرية</span><span class="sxs-lookup"><span data-stu-id="392fd-313">Military Service Number</span></span>
- <span data-ttu-id="392fd-314">معرف الوردية (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-314">Shift ID (required)</span></span>
- <span data-ttu-id="392fd-315">رقم الضريبة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-315">Tax Number (required)</span></span>
- <span data-ttu-id="392fd-316">معرّف الاتحاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-316">Union ID (required)</span></span>
- <span data-ttu-id="392fd-317">معرّف يوم العمل (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-317">Work Day ID (required)</span></span>
- <span data-ttu-id="392fd-318">رقم تصريح العمل</span><span class="sxs-lookup"><span data-stu-id="392fd-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="392fd-319">بالنسبة إلى طريقة الدفع، تدعم المكسيك الدفع **نقدًا** وبواسطة **شيك** (الشيك الفعلي للمؤسسة) و**الدفع الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="392fd-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="392fd-320">إذا لم يتم تحديد أي طريقة دفع، فسيتم استخدام **الشيك** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="392fd-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="392fd-321">تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="392fd-321">Employment details</span></span>

<span data-ttu-id="392fd-322">يتم استخدام سجل تفاصيل التوظيف كمعلومات أساسية لاستخراج حالات تعيين موظف وإنهاء خدماته وإعادة تعيينه في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="392fd-323">تدعم خدمة Dayforce سجل توظيف نشط واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="392fd-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="392fd-324">تاريخ بدء التوظيف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-324">Employment start date (required)</span></span>
- <span data-ttu-id="392fd-325">تاريخ انتهاء التوظيف</span><span class="sxs-lookup"><span data-stu-id="392fd-325">Employment end date</span></span>
- <span data-ttu-id="392fd-326">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="392fd-326">Start date</span></span>
- <span data-ttu-id="392fd-327">تاريخ البدء المعدل</span><span class="sxs-lookup"><span data-stu-id="392fd-327">Adjusted start date</span></span>
- <span data-ttu-id="392fd-328">تاريخ إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="392fd-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="392fd-329">سبب إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="392fd-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="392fd-330">يتم استخراج التواريخ الأساسية للموظف باستخدام المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="392fd-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="392fd-331">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-331">Human Resources</span></span>                | <span data-ttu-id="392fd-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392fd-333">أقرب تاريخ توظيف</span><span class="sxs-lookup"><span data-stu-id="392fd-333">Most recent hire date</span></span> | <span data-ttu-id="392fd-334">تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="392fd-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="392fd-335">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="392fd-335">Termination date</span></span>      | <span data-ttu-id="392fd-336">تاريخ انتهاء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="392fd-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="392fd-337">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="392fd-337">Start date</span></span>            | <span data-ttu-id="392fd-338">تاريخ البدء المعدل أو تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي غير النشط</span><span class="sxs-lookup"><span data-stu-id="392fd-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="392fd-339">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="392fd-339">Original hire date</span></span>    | <span data-ttu-id="392fd-340">تاريخ بدء التوظيف في سجل محفوظات التوظيف الأحدث</span><span class="sxs-lookup"><span data-stu-id="392fd-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="392fd-341">التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-341">Compensation</span></span>

<span data-ttu-id="392fd-342">يجب إقران خطة تعويض ثابت بالمنصب الأساسي لكل موظف خلال فترة التوظيف.</span><span class="sxs-lookup"><span data-stu-id="392fd-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="392fd-343">تبدأ هذه الفترة الزمنية في التاريخ الذي تم تعيين الموظف فيه (أو تاريخ بدء التوظيف) وتستمر حتى إنهاء خدمة الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="392fd-344">تاريخ السريان (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-344">Effective Date (required)</span></span>
- <span data-ttu-id="392fd-345">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="392fd-345">Expiration date</span></span>
- <span data-ttu-id="392fd-346">معدل الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-346">Pay Rate (required)</span></span>
- <span data-ttu-id="392fd-347">تحويلات ‏‫معدل الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="392fd-348">المكافئ السنوي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="392fd-349">المكافئ الساعي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="392fd-350">إذا كان لدى موظف ساعي مناصب متعددة، فسيتم استيراد التعويض الثابت للمنصب الأساسي إلى Dayforce كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="392fd-351">فيما يتعلق بالمناصب غير الأساسية، يُحفظ المعدل الساعي إلى المنصب المناظر في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="392fd-352">إذا كان لدى موظف يتلقى راتبًا مناصب متعددة، فسيتم استخراج المعدل الساعي التراكمي والراتب السنوي عبر كافة المناصب النشطة، وسيتم استخدامها كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="392fd-353">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="392fd-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="392fd-354">معرّف الضمان الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="392fd-354">Social Security identifier</span></span> 

<span data-ttu-id="392fd-355">يجب أن يكون لدى كل موظف معرّفًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="392fd-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="392fd-356">يجب أن يكون هذا المعرّف من نوع التعريف‬ **SSN**.</span><span class="sxs-lookup"><span data-stu-id="392fd-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="392fd-357">في Dayforce، يتم استخراجه تلقائيًا على أنه معرّف الضمان الاجتماعي للموظف المطلوب للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="392fd-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="392fd-358">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-358">Primary (required)</span></span>
- <span data-ttu-id="392fd-359">نوع التعريف = "SSN"</span><span class="sxs-lookup"><span data-stu-id="392fd-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="392fd-360">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="392fd-360">Issued Date</span></span>
- <span data-ttu-id="392fd-361">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="392fd-361">Expiration Date</span></span>

<span data-ttu-id="392fd-362">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **SSN**.</span><span class="sxs-lookup"><span data-stu-id="392fd-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="392fd-363">ومع ذلك، فإن السجل الذي سيتم دمجه في Dayforce هو فقط الذي يحمل العلامة **أساسي**، بصرف النظر عما إذا كان الرقم نشطًا أو منتهي الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="392fd-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="392fd-364">الحسابات البنكية والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="392fd-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="392fd-365">يجب إدخال معلومات صالحة حول الحساب البنكي لأي موظف يختار تلقي الدفع من خلال تحويلات إلى الحساب البنكي‬.</span><span class="sxs-lookup"><span data-stu-id="392fd-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="392fd-366">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-366">Human Resources</span></span>                         | <span data-ttu-id="392fd-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392fd-368">رقم الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="392fd-369">رمز SWIFT (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-369">SWIFT code (required)</span></span>          | <span data-ttu-id="392fd-370">حقل **معرّف البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="392fd-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="392fd-371">رقم الفرع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="392fd-372">نوع الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-372">Bank account type (required)</span></span>   | <span data-ttu-id="392fd-373">حقل **نوع البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="392fd-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="392fd-374">تتضمن القيم المدعومة **شيكات** و**كشف المرتبات**.</span><span class="sxs-lookup"><span data-stu-id="392fd-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="392fd-375">يتعين على الموظفين الذين اختاروا تلقي الدفع عبر تحويلات إلى الحساب البنكي‬ توفير ارتباط إلى حساب متبقٍ موجود ضمن كيان قانوني عنوانه الأساسي في المكسيك ويقترن بحساب بنكي صالح من بنك مكسيكي.</span><span class="sxs-lookup"><span data-stu-id="392fd-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="392fd-376">يتم تجاهل كافة الحسابات الأخرى غير الحسابات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="392fd-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="392fd-377">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="392fd-377">Address information</span></span>

<span data-ttu-id="392fd-378">يجب أن يكون لدى كل موظف موقعًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="392fd-378">Every employee must have one primary location.</span></span> <span data-ttu-id="392fd-379">في Dayforce، يتم استخدام هذا الموقع لتحديد مكان الإقامة الأساسي للموظف لأغراض ضريبية.</span><span class="sxs-lookup"><span data-stu-id="392fd-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="392fd-380">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-380">Primary (required)</span></span>
- <span data-ttu-id="392fd-381">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-381">Country/region (required)</span></span>
- <span data-ttu-id="392fd-382">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="392fd-383">الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-383">Street (required)</span></span>
- <span data-ttu-id="392fd-384">رقم الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-384">Street Number (required)</span></span>
- <span data-ttu-id="392fd-385">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="392fd-385">Building Complement</span></span>
- <span data-ttu-id="392fd-386">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-386">City (required)</span></span>
- <span data-ttu-id="392fd-387">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-387">State (required)</span></span>
- <span data-ttu-id="392fd-388">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="392fd-389">تكوين البيانات لإنشاء كشف مرتبات في الولايات المتحدة وكندا</span><span class="sxs-lookup"><span data-stu-id="392fd-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="392fd-390">إذا كنت تقوم بإنشاء الدفع للموظفين في الولايات المتحدة وكندا، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="392fd-391">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="392fd-391">Departments are required on positions.</span></span>
- <span data-ttu-id="392fd-392">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="392fd-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="392fd-393">يمكنك تكوين لـ Human Resourcesمطالبة المناصب بتحديد قسم.</span><span class="sxs-lookup"><span data-stu-id="392fd-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="392fd-394">للقيام بذلك، انتقل إلى **الموارد البشرية المناصب المشتركة > المناصب > الأقسام مطلوبة على المناصب**.</span><span class="sxs-lookup"><span data-stu-id="392fd-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="392fd-395">من المستحسن أن يتم فرض هذا الإعداد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="392fd-396">أنواع الوظائف</span><span class="sxs-lookup"><span data-stu-id="392fd-396">Job types</span></span>

<span data-ttu-id="392fd-397">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="392fd-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="392fd-398">تعتبر أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في الولايات المتحدة وكندا.</span><span class="sxs-lookup"><span data-stu-id="392fd-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="392fd-399">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="392fd-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="392fd-400">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="392fd-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="392fd-401">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="392fd-402">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="392fd-402">Job type</span></span>   | <span data-ttu-id="392fd-403">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="392fd-404">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="392fd-404">Hourly</span></span>     | <span data-ttu-id="392fd-405">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="392fd-405">Hourly</span></span>      |
| <span data-ttu-id="392fd-406">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="392fd-406">Salaried</span></span>   | <span data-ttu-id="392fd-407">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="392fd-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="392fd-408">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="392fd-408">Position types</span></span> 

<span data-ttu-id="392fd-409">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="392fd-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="392fd-410">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="392fd-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="392fd-411">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="392fd-412">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="392fd-412">Position type</span></span>   | <span data-ttu-id="392fd-413">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="392fd-414">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="392fd-414">Full-time</span></span>       | <span data-ttu-id="392fd-415">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="392fd-415">Full time employee</span></span> |
| <span data-ttu-id="392fd-416">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="392fd-416">Part-time</span></span>       | <span data-ttu-id="392fd-417">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="392fd-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="392fd-418">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="392fd-418">Reason codes</span></span>

<span data-ttu-id="392fd-419">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="392fd-420">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="392fd-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="392fd-421">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="392fd-422">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="392fd-422">Reason code</span></span>    | <span data-ttu-id="392fd-423">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-423">Description</span></span>      | <span data-ttu-id="392fd-424">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="392fd-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="392fd-425">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="392fd-425">RESIGNATION</span></span>    | <span data-ttu-id="392fd-426">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="392fd-426">Resignation</span></span>      | <span data-ttu-id="392fd-427">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-427">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-428">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="392fd-428">TERMINATION</span></span>    | <span data-ttu-id="392fd-429">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="392fd-429">Termination</span></span>      | <span data-ttu-id="392fd-430">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-430">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-431">التقاعد</span><span class="sxs-lookup"><span data-stu-id="392fd-431">RETIREMENT</span></span>     | <span data-ttu-id="392fd-432">التقاعد</span><span class="sxs-lookup"><span data-stu-id="392fd-432">Retirement</span></span>       | <span data-ttu-id="392fd-433">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-433">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-434">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="392fd-434">OTHER</span></span>          | <span data-ttu-id="392fd-435">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="392fd-435">Other Reasons</span></span>    | <span data-ttu-id="392fd-436">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-436">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-437">الوفاة</span><span class="sxs-lookup"><span data-stu-id="392fd-437">DEATH</span></span>          | <span data-ttu-id="392fd-438">الوفاة</span><span class="sxs-lookup"><span data-stu-id="392fd-438">Death</span></span>            | <span data-ttu-id="392fd-439">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-439">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="392fd-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="392fd-441">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="392fd-441">Leave of Absence</span></span> | <span data-ttu-id="392fd-442">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-442">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="392fd-443">CONTRACTEND</span></span>    | <span data-ttu-id="392fd-444">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="392fd-444">End of Contract</span></span>  | <span data-ttu-id="392fd-445">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-445">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="392fd-446">SALARYCHANGE</span></span>   | <span data-ttu-id="392fd-447">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="392fd-447">Change of Salary</span></span> | <span data-ttu-id="392fd-448">التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="392fd-449">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="392fd-449">Marital status</span></span>

<span data-ttu-id="392fd-450">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="392fd-451">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="392fd-452">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-452">Human Resources</span></span>                 | <span data-ttu-id="392fd-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="392fd-454">متزوج</span><span class="sxs-lookup"><span data-stu-id="392fd-454">Married</span></span>                | <span data-ttu-id="392fd-455">متزوج</span><span class="sxs-lookup"><span data-stu-id="392fd-455">Married</span></span>              |
| <span data-ttu-id="392fd-456">أعزب</span><span class="sxs-lookup"><span data-stu-id="392fd-456">Single</span></span>                 | <span data-ttu-id="392fd-457">أعزب</span><span class="sxs-lookup"><span data-stu-id="392fd-457">Single</span></span>               |
| <span data-ttu-id="392fd-458">أرمل</span><span class="sxs-lookup"><span data-stu-id="392fd-458">Widowed</span></span>                | <span data-ttu-id="392fd-459">أرمل</span><span class="sxs-lookup"><span data-stu-id="392fd-459">Widowed</span></span>              |
| <span data-ttu-id="392fd-460">مطلق</span><span class="sxs-lookup"><span data-stu-id="392fd-460">Divorced</span></span>               | <span data-ttu-id="392fd-461">مطلق</span><span class="sxs-lookup"><span data-stu-id="392fd-461">Divorced</span></span>             |
| <span data-ttu-id="392fd-462">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="392fd-462">Registered Partnership</span></span> | <span data-ttu-id="392fd-463">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="392fd-463">Domestic Partnership</span></span> |
| <span data-ttu-id="392fd-464">بلا</span><span class="sxs-lookup"><span data-stu-id="392fd-464">None</span></span>                   | <span data-ttu-id="392fd-465">بلا</span><span class="sxs-lookup"><span data-stu-id="392fd-465">None</span></span>                 |
| <span data-ttu-id="392fd-466">تعايش</span><span class="sxs-lookup"><span data-stu-id="392fd-466">Cohabiting</span></span>             | <span data-ttu-id="392fd-467">تعايش</span><span class="sxs-lookup"><span data-stu-id="392fd-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="392fd-468">الجنس</span><span class="sxs-lookup"><span data-stu-id="392fd-468">Gender</span></span>

<span data-ttu-id="392fd-469">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="392fd-470">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="392fd-471">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-471">Human Resources</span></span>       | <span data-ttu-id="392fd-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="392fd-473">ذكر</span><span class="sxs-lookup"><span data-stu-id="392fd-473">Male</span></span>         | <span data-ttu-id="392fd-474">ذكر</span><span class="sxs-lookup"><span data-stu-id="392fd-474">Male</span></span>            |
| <span data-ttu-id="392fd-475">أنثى</span><span class="sxs-lookup"><span data-stu-id="392fd-475">Female</span></span>       | <span data-ttu-id="392fd-476">أنثى</span><span class="sxs-lookup"><span data-stu-id="392fd-476">Female</span></span>          |
| <span data-ttu-id="392fd-477">غير محدد</span><span class="sxs-lookup"><span data-stu-id="392fd-477">Non-specific</span></span> | <span data-ttu-id="392fd-478">*غير مدعوم*</span><span class="sxs-lookup"><span data-stu-id="392fd-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="392fd-479">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-479">Earning codes</span></span>

<span data-ttu-id="392fd-480">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="392fd-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="392fd-481">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="392fd-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="392fd-482">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="392fd-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="392fd-483">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="392fd-483">Supported frequencies</span></span>

- <span data-ttu-id="392fd-484">الكل</span><span class="sxs-lookup"><span data-stu-id="392fd-484">All</span></span>
- <span data-ttu-id="392fd-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="392fd-485">EVERYPAY</span></span>
- <span data-ttu-id="392fd-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="392fd-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="392fd-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="392fd-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="392fd-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="392fd-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="392fd-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-489">1OFMTH</span></span>
- <span data-ttu-id="392fd-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-490">LASTOFMTH</span></span>
- <span data-ttu-id="392fd-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-491">2OFMTH</span></span>
- <span data-ttu-id="392fd-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-492">3OFMTH</span></span>
- <span data-ttu-id="392fd-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-493">4OFMTH</span></span>
- <span data-ttu-id="392fd-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-494">5OFMTH</span></span>
- <span data-ttu-id="392fd-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-495">1N2OFMTH</span></span>
- <span data-ttu-id="392fd-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-496">3N4OFMTH</span></span>
- <span data-ttu-id="392fd-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-497">1N3OFMTH</span></span>
- <span data-ttu-id="392fd-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-498">1N4OFMTH</span></span>
- <span data-ttu-id="392fd-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-499">2N3OFMTH</span></span>
- <span data-ttu-id="392fd-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-500">2N4OFMTH</span></span>
- <span data-ttu-id="392fd-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="392fd-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="392fd-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="392fd-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="392fd-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="392fd-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="392fd-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="392fd-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="392fd-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="392fd-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="392fd-513">العناوين</span><span class="sxs-lookup"><span data-stu-id="392fd-513">Addresses</span></span>

<span data-ttu-id="392fd-514">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="392fd-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="392fd-515">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="392fd-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="392fd-516">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-516">Human Resources</span></span>          | <span data-ttu-id="392fd-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="392fd-518">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="392fd-518">Country/Region</span></span>  | <span data-ttu-id="392fd-519">كود البلد</span><span class="sxs-lookup"><span data-stu-id="392fd-519">Country Code</span></span>          |
| <span data-ttu-id="392fd-520">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="392fd-520">Zip/Postal Code</span></span> | <span data-ttu-id="392fd-521">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="392fd-521">Postal Code</span></span>           |
| <span data-ttu-id="392fd-522">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="392fd-522">State</span></span>           | <span data-ttu-id="392fd-523">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="392fd-523">State Code</span></span>            |
| <span data-ttu-id="392fd-524">المدينة</span><span class="sxs-lookup"><span data-stu-id="392fd-524">City</span></span>            | <span data-ttu-id="392fd-525">المدينة</span><span class="sxs-lookup"><span data-stu-id="392fd-525">City</span></span>                  |
| <span data-ttu-id="392fd-526">الإقليم</span><span class="sxs-lookup"><span data-stu-id="392fd-526">County</span></span>          | <span data-ttu-id="392fd-527">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="392fd-527">County (Municipality)</span></span> |
| <span data-ttu-id="392fd-528">الشارع</span><span class="sxs-lookup"><span data-stu-id="392fd-528">Street</span></span>          | <span data-ttu-id="392fd-529">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="392fd-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="392fd-530">مناطق الضريبة</span><span class="sxs-lookup"><span data-stu-id="392fd-530">Tax regions</span></span>

<span data-ttu-id="392fd-531">تُستخدم مناطق الضريبة لتحديد الضريبة المناسبة التي يجب تطبيقها أثناء إنشاء كشف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="392fd-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="392fd-532">يتم تعيين مناطق الضريبة إلى Dayforce كعناوين موقع.</span><span class="sxs-lookup"><span data-stu-id="392fd-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="392fd-533">يجب أن تكون منطقة الضريبة الافتراضية مقترنة بمنصب العامل النشط.</span><span class="sxs-lookup"><span data-stu-id="392fd-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="392fd-534">منطقة الضريبة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-534">Tax region (required)</span></span>
- <span data-ttu-id="392fd-535">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="392fd-535">Country/Region (required)</span></span>
- <span data-ttu-id="392fd-536">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-536">State (required)</span></span>
- <span data-ttu-id="392fd-537">الإقليم</span><span class="sxs-lookup"><span data-stu-id="392fd-537">County</span></span> 
- <span data-ttu-id="392fd-538">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="392fd-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="392fd-539">تكوين بياناتك لإنشاء كشف المرتبات في المكسيك</span><span class="sxs-lookup"><span data-stu-id="392fd-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="392fd-540">إذا كنت تقوم بإنشاء الدفع للموظفين في المكسيك، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="392fd-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="392fd-541">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="392fd-541">Departments are required on positions.</span></span>
- <span data-ttu-id="392fd-542">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="392fd-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="392fd-543">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="392fd-543">Job types</span></span>

<span data-ttu-id="392fd-544">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="392fd-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="392fd-545">أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="392fd-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="392fd-546">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="392fd-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="392fd-547">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="392fd-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="392fd-548">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="392fd-549">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="392fd-549">Job type</span></span>   | <span data-ttu-id="392fd-550">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="392fd-551">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="392fd-551">Hourly</span></span>     | <span data-ttu-id="392fd-552">الحد الأقصى للأجر في الساعة‬</span><span class="sxs-lookup"><span data-stu-id="392fd-552">MX Hourly</span></span>   |
| <span data-ttu-id="392fd-553">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="392fd-553">Salaried</span></span>   | <span data-ttu-id="392fd-554">الحد الأقصى للراتب</span><span class="sxs-lookup"><span data-stu-id="392fd-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="392fd-555">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="392fd-555">Position types</span></span> 

<span data-ttu-id="392fd-556">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="392fd-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="392fd-557">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="392fd-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="392fd-558">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="392fd-559">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="392fd-559">Position type</span></span>   | <span data-ttu-id="392fd-560">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="392fd-561">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="392fd-561">Full-time</span></span>       | <span data-ttu-id="392fd-562">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="392fd-562">Full time employee</span></span> |
| <span data-ttu-id="392fd-563">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="392fd-563">Part-time</span></span>       | <span data-ttu-id="392fd-564">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="392fd-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="392fd-565">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="392fd-565">Reason codes</span></span>

<span data-ttu-id="392fd-566">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="392fd-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="392fd-567">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="392fd-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="392fd-568">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="392fd-569">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="392fd-569">Reason code</span></span>            | <span data-ttu-id="392fd-570">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-570">Description</span></span>                    | <span data-ttu-id="392fd-571">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="392fd-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="392fd-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="392fd-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="392fd-573">المغادرة قبل كشف المرتبات الأول</span><span class="sxs-lookup"><span data-stu-id="392fd-573">Departure before first payroll</span></span> | <span data-ttu-id="392fd-574">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-574">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-575">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="392fd-575">RESIGNATION</span></span>            | <span data-ttu-id="392fd-576">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="392fd-576">Resignation</span></span>                    | <span data-ttu-id="392fd-577">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-577">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-578">المعاش</span><span class="sxs-lookup"><span data-stu-id="392fd-578">PENSION</span></span>                | <span data-ttu-id="392fd-579">المعاش</span><span class="sxs-lookup"><span data-stu-id="392fd-579">Pension</span></span>                        | <span data-ttu-id="392fd-580">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-580">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-581">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="392fd-581">TERMINATION</span></span>            | <span data-ttu-id="392fd-582">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="392fd-582">Termination</span></span>                    | <span data-ttu-id="392fd-583">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-583">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-584">التقاعد</span><span class="sxs-lookup"><span data-stu-id="392fd-584">RETIREMENT</span></span>             | <span data-ttu-id="392fd-585">التقاعد</span><span class="sxs-lookup"><span data-stu-id="392fd-585">Retirement</span></span>                     | <span data-ttu-id="392fd-586">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-586">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-587">الغائب</span><span class="sxs-lookup"><span data-stu-id="392fd-587">ABSENTEE</span></span>               | <span data-ttu-id="392fd-588">الغائب</span><span class="sxs-lookup"><span data-stu-id="392fd-588">Absentee</span></span>                       | <span data-ttu-id="392fd-589">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-589">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-590">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="392fd-590">OTHER</span></span>                  | <span data-ttu-id="392fd-591">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="392fd-591">Other Reasons</span></span>                  | <span data-ttu-id="392fd-592">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-592">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-593">إقفال</span><span class="sxs-lookup"><span data-stu-id="392fd-593">CLOSURE</span></span>                | <span data-ttu-id="392fd-594">إقفال الشركة</span><span class="sxs-lookup"><span data-stu-id="392fd-594">Business Closure</span></span>               | <span data-ttu-id="392fd-595">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-595">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-596">الوفاة</span><span class="sxs-lookup"><span data-stu-id="392fd-596">DEATH</span></span>                  | <span data-ttu-id="392fd-597">الوفاة</span><span class="sxs-lookup"><span data-stu-id="392fd-597">Death</span></span>                          | <span data-ttu-id="392fd-598">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-598">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="392fd-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="392fd-600">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="392fd-600">Leave of Absence</span></span>               | <span data-ttu-id="392fd-601">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-601">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="392fd-602">CONTRACTEND</span></span>            | <span data-ttu-id="392fd-603">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="392fd-603">End of Contract</span></span>                | <span data-ttu-id="392fd-604">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="392fd-604">Terminate worker</span></span>     |
| <span data-ttu-id="392fd-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="392fd-605">SALARYCHANGE</span></span>           | <span data-ttu-id="392fd-606">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="392fd-606">Change of Salary</span></span>               | <span data-ttu-id="392fd-607">التعويض</span><span class="sxs-lookup"><span data-stu-id="392fd-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="392fd-608">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="392fd-608">Terms of employment</span></span>

<span data-ttu-id="392fd-609">يتم استخدام شروط التوظيف لإنشاء فئات شروط التوظيف.</span><span class="sxs-lookup"><span data-stu-id="392fd-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="392fd-610">يتم تعيين الشروط إلى Dayforce كقيم مؤشر التوظيف.</span><span class="sxs-lookup"><span data-stu-id="392fd-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="392fd-611">شروط التوظيف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="392fd-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="392fd-612">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="392fd-612">Terms of employment</span></span>   | <span data-ttu-id="392fd-613">الوصف</span><span class="sxs-lookup"><span data-stu-id="392fd-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="392fd-614">عادي</span><span class="sxs-lookup"><span data-stu-id="392fd-614">Regular</span></span>               | <span data-ttu-id="392fd-615">عادي</span><span class="sxs-lookup"><span data-stu-id="392fd-615">Regular</span></span>     |
| <span data-ttu-id="392fd-616">مباشر</span><span class="sxs-lookup"><span data-stu-id="392fd-616">Direct</span></span>                | <span data-ttu-id="392fd-617">مباشر</span><span class="sxs-lookup"><span data-stu-id="392fd-617">Direct</span></span>      |
| <span data-ttu-id="392fd-618">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="392fd-618">Internship</span></span>            | <span data-ttu-id="392fd-619">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="392fd-619">Internship</span></span>  |
| <span data-ttu-id="392fd-620">دائم</span><span class="sxs-lookup"><span data-stu-id="392fd-620">Permanent</span></span>             | <span data-ttu-id="392fd-621">دائم</span><span class="sxs-lookup"><span data-stu-id="392fd-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="392fd-622">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="392fd-622">Marital status</span></span>

<span data-ttu-id="392fd-623">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="392fd-624">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="392fd-625">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-625">Human Resources</span></span>                 | <span data-ttu-id="392fd-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="392fd-627">متزوج</span><span class="sxs-lookup"><span data-stu-id="392fd-627">Married</span></span>                | <span data-ttu-id="392fd-628">متزوج</span><span class="sxs-lookup"><span data-stu-id="392fd-628">Married</span></span>                   |
| <span data-ttu-id="392fd-629">أعزب</span><span class="sxs-lookup"><span data-stu-id="392fd-629">Single</span></span>                 | <span data-ttu-id="392fd-630">أعزب</span><span class="sxs-lookup"><span data-stu-id="392fd-630">Single</span></span>                    |
| <span data-ttu-id="392fd-631">أرمل</span><span class="sxs-lookup"><span data-stu-id="392fd-631">Widowed</span></span>                | <span data-ttu-id="392fd-632">أرمل</span><span class="sxs-lookup"><span data-stu-id="392fd-632">Widowed</span></span>                   |
| <span data-ttu-id="392fd-633">مطلق</span><span class="sxs-lookup"><span data-stu-id="392fd-633">Divorced</span></span>               | <span data-ttu-id="392fd-634">مطلق</span><span class="sxs-lookup"><span data-stu-id="392fd-634">Divorced</span></span>                  |
| <span data-ttu-id="392fd-635">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="392fd-635">Registered Partnership</span></span> | <span data-ttu-id="392fd-636">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="392fd-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="392fd-637">بلا</span><span class="sxs-lookup"><span data-stu-id="392fd-637">None</span></span>                   | <span data-ttu-id="392fd-638">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="392fd-639">تعايش</span><span class="sxs-lookup"><span data-stu-id="392fd-639">Cohabiting</span></span>             | <span data-ttu-id="392fd-640">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="392fd-641">الجنس</span><span class="sxs-lookup"><span data-stu-id="392fd-641">Gender</span></span>

<span data-ttu-id="392fd-642">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="392fd-643">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="392fd-644">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-644">Human Resources</span></span>       | <span data-ttu-id="392fd-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="392fd-646">ذكر</span><span class="sxs-lookup"><span data-stu-id="392fd-646">Male</span></span>         | <span data-ttu-id="392fd-647">ذكر</span><span class="sxs-lookup"><span data-stu-id="392fd-647">Male</span></span>                      |
| <span data-ttu-id="392fd-648">أنثى</span><span class="sxs-lookup"><span data-stu-id="392fd-648">Female</span></span>       | <span data-ttu-id="392fd-649">أنثى</span><span class="sxs-lookup"><span data-stu-id="392fd-649">Female</span></span>                    |
| <span data-ttu-id="392fd-650">غير محدد</span><span class="sxs-lookup"><span data-stu-id="392fd-650">Non-specific</span></span> | <span data-ttu-id="392fd-651">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="392fd-652">أسلوب الدفع</span><span class="sxs-lookup"><span data-stu-id="392fd-652">Payment method</span></span>

<span data-ttu-id="392fd-653">تقدم طرق دفع للموظف والشركة طريقة لوصف كيفية تسديد مرتبات وأجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="392fd-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="392fd-654">يتم تعيين طرق الدفع إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="392fd-655">يعرض الجدول التالي كيفية تعيين طرق الدفع إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="392fd-656">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-656">Human Resources</span></span>             | <span data-ttu-id="392fd-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="392fd-658">نقدي</span><span class="sxs-lookup"><span data-stu-id="392fd-658">Cash</span></span>               | <span data-ttu-id="392fd-659">نقدي</span><span class="sxs-lookup"><span data-stu-id="392fd-659">Cash</span></span>                      |
| <span data-ttu-id="392fd-660">دفع إلكتروني</span><span class="sxs-lookup"><span data-stu-id="392fd-660">Electronic Payment</span></span> | <span data-ttu-id="392fd-661">التحويل</span><span class="sxs-lookup"><span data-stu-id="392fd-661">Transfer</span></span>                  |
| <span data-ttu-id="392fd-662">فحص</span><span class="sxs-lookup"><span data-stu-id="392fd-662">Check</span></span>              | <span data-ttu-id="392fd-663">شيك</span><span class="sxs-lookup"><span data-stu-id="392fd-663">Cheque</span></span>                    |
| <span data-ttu-id="392fd-664">حوالة مصرفية</span><span class="sxs-lookup"><span data-stu-id="392fd-664">Bank Draft</span></span>         | <span data-ttu-id="392fd-665">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="392fd-666">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="392fd-666">Other</span></span>              | <span data-ttu-id="392fd-667">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="392fd-668">نوع الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="392fd-668">Bank account type</span></span>

<span data-ttu-id="392fd-669">يتم استخدام أنواع الحسابات البنكية للدفع الإلكتروني للموظفين.</span><span class="sxs-lookup"><span data-stu-id="392fd-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="392fd-670">يتم تعيين أنواع الحسابات البنكية إلى Dayforce كمعلومات حساب التحويل.</span><span class="sxs-lookup"><span data-stu-id="392fd-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="392fd-671">وتتم ترجمة أنواع الحسابات البنكية، كما هو مناسب، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="392fd-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="392fd-672">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-672">Human Resources</span></span>            | <span data-ttu-id="392fd-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="392fd-674">حساب شيكات</span><span class="sxs-lookup"><span data-stu-id="392fd-674">Checking Account</span></span>  | <span data-ttu-id="392fd-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="392fd-675">CheckingAccount</span></span>           |
| <span data-ttu-id="392fd-676">حساب الراتب</span><span class="sxs-lookup"><span data-stu-id="392fd-676">Payroll Account</span></span>   | <span data-ttu-id="392fd-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="392fd-677">PayrollAccount</span></span>            |
| <span data-ttu-id="392fd-678">حساب توفير</span><span class="sxs-lookup"><span data-stu-id="392fd-678">Savings Account</span></span>   | <span data-ttu-id="392fd-679">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="392fd-680">حساب BankGirot</span><span class="sxs-lookup"><span data-stu-id="392fd-680">BankGirot account</span></span> | <span data-ttu-id="392fd-681">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="392fd-682">حساب PlusGirot</span><span class="sxs-lookup"><span data-stu-id="392fd-682">PlusGirot account</span></span> | <span data-ttu-id="392fd-683">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="392fd-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="392fd-684">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="392fd-684">Earning codes</span></span>

<span data-ttu-id="392fd-685">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="392fd-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="392fd-686">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="392fd-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="392fd-687">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="392fd-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="392fd-688">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="392fd-688">Supported frequencies</span></span>

- <span data-ttu-id="392fd-689">الكل</span><span class="sxs-lookup"><span data-stu-id="392fd-689">All</span></span>
- <span data-ttu-id="392fd-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="392fd-690">EVERYPAY</span></span>
- <span data-ttu-id="392fd-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="392fd-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="392fd-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="392fd-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="392fd-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="392fd-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="392fd-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-694">1OFMTH</span></span>
- <span data-ttu-id="392fd-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-695">LASTOFMTH</span></span>
- <span data-ttu-id="392fd-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-696">2OFMTH</span></span>
- <span data-ttu-id="392fd-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-697">3OFMTH</span></span>
- <span data-ttu-id="392fd-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-698">4OFMTH</span></span>
- <span data-ttu-id="392fd-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-699">5OFMTH</span></span>
- <span data-ttu-id="392fd-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-700">1N2OFMTH</span></span>
- <span data-ttu-id="392fd-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-701">3N4OFMTH</span></span>
- <span data-ttu-id="392fd-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-702">1N3OFMTH</span></span>
- <span data-ttu-id="392fd-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-703">1N4OFMTH</span></span>
- <span data-ttu-id="392fd-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-704">2N3OFMTH</span></span>
- <span data-ttu-id="392fd-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-705">2N4OFMTH</span></span>
- <span data-ttu-id="392fd-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="392fd-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="392fd-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="392fd-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="392fd-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="392fd-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="392fd-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="392fd-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="392fd-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="392fd-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="392fd-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="392fd-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="392fd-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="392fd-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="392fd-718">العناوين</span><span class="sxs-lookup"><span data-stu-id="392fd-718">Addresses</span></span>

<span data-ttu-id="392fd-719">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="392fd-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="392fd-720">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="392fd-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="392fd-721">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="392fd-721">Human Resources</span></span>              | <span data-ttu-id="392fd-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="392fd-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="392fd-723">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="392fd-723">Country/Region</span></span>      | <span data-ttu-id="392fd-724">كود البلد</span><span class="sxs-lookup"><span data-stu-id="392fd-724">Country Code</span></span>          |
| <span data-ttu-id="392fd-725">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="392fd-725">Zip/Postal Code</span></span>     | <span data-ttu-id="392fd-726">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="392fd-726">Postal Code</span></span>           |
| <span data-ttu-id="392fd-727">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="392fd-727">State</span></span>               | <span data-ttu-id="392fd-728">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="392fd-728">State Code</span></span>            |
| <span data-ttu-id="392fd-729">المدينة</span><span class="sxs-lookup"><span data-stu-id="392fd-729">City</span></span>                | <span data-ttu-id="392fd-730">المدينة</span><span class="sxs-lookup"><span data-stu-id="392fd-730">City</span></span>                  |
| <span data-ttu-id="392fd-731">الإقليم</span><span class="sxs-lookup"><span data-stu-id="392fd-731">County</span></span>              | <span data-ttu-id="392fd-732">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="392fd-732">County (Municipality)</span></span> |
| <span data-ttu-id="392fd-733">الشارع</span><span class="sxs-lookup"><span data-stu-id="392fd-733">Street</span></span>              | <span data-ttu-id="392fd-734">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="392fd-734">Address Line 1</span></span>        |
| <span data-ttu-id="392fd-735">رقم الشارع</span><span class="sxs-lookup"><span data-stu-id="392fd-735">Street Number</span></span>       | <span data-ttu-id="392fd-736">سطر العنوان 2</span><span class="sxs-lookup"><span data-stu-id="392fd-736">Address Line 2</span></span>        |
| <span data-ttu-id="392fd-737">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="392fd-737">Building Complement</span></span> | <span data-ttu-id="392fd-738">سطر العنوان 5</span><span class="sxs-lookup"><span data-stu-id="392fd-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="392fd-739">رقم جواز السفر</span><span class="sxs-lookup"><span data-stu-id="392fd-739">Passport number</span></span>

<span data-ttu-id="392fd-740">بإمكان الموظفين إعلان معلومات جواز السفر.</span><span class="sxs-lookup"><span data-stu-id="392fd-740">Employees can declare passport information.</span></span> <span data-ttu-id="392fd-741">هذه المعلومات هي نوع من أنواع تعريف **جواز السفر** وهي تتكامل في Dayforce كجزء من معلومات الموظف خاصة بالمكسيك.</span><span class="sxs-lookup"><span data-stu-id="392fd-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="392fd-742">نوع التعريف = "جواز سفر"</span><span class="sxs-lookup"><span data-stu-id="392fd-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="392fd-743">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="392fd-743">Issued Date</span></span>
- <span data-ttu-id="392fd-744">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="392fd-744">Expiration Date</span></span>

<span data-ttu-id="392fd-745">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **جواز سفر**.</span><span class="sxs-lookup"><span data-stu-id="392fd-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="392fd-746">ومع ذلك، يتم دمج إدخال جواز السفر النشط الحالي فقط في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="392fd-747">إذا انتهت صلاحية جميع إدخالات جوازات السفر، فسيتكامل جواز السفر الذي تم إصداره مؤخرًا في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="392fd-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

