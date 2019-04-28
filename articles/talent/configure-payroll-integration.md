---
title: تكوين تكامل كشف المرتبات بين Talent وDayforce
description: يشرح هذا الموضوع كيفية تكوين التكامل بين Microsoft Dynamics 365 for Talent وCeridian Dayforce لكي تتمكن من معالجة دورة دفع.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
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
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/26/2019
ms.locfileid: "898434"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="b0641-103">تكوين تكامل كشف الرواتب بين Talent وDayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0641-104">يعتمد التكامل بين Dynamics 365 for Talent وCeridian Dayforce على العديد من خطوات التكوين التي تم وصفها في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b0641-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="b0641-105">يجب عليك تكوين التكامل في كل من Talent وDayforce قبل أن تتمكن من معالجة دورة دفع.</span><span class="sxs-lookup"><span data-stu-id="b0641-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b0641-106">عندما تستخدم خدمة مثل Dayforce لإتمام دورات الدفع، يجب عليك تمكين التكامل في Talent.</span><span class="sxs-lookup"><span data-stu-id="b0641-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="b0641-107">يتطلب التكامل بيانات معينة من Talent.</span><span class="sxs-lookup"><span data-stu-id="b0641-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="b0641-108">لذلك، يجب عليك التأكد من أن البيانات التي تم تعيينها إلى Dayforce هي بيانات تم تكوينها في Talent بطريقة تدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="b0641-109">يستخدم التكامل الفئات الواسعة التالية من البيانات:</span><span class="sxs-lookup"><span data-stu-id="b0641-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b0641-110">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b0641-110">Human resources data</span></span>
- <span data-ttu-id="b0641-111">بيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-111">Compensation data</span></span>
- <span data-ttu-id="b0641-112">بيانات كشف المرتبات، مثل دورات الدفع وفترات الدفع وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b0641-113">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-113">Worker data</span></span>

<span data-ttu-id="b0641-114">يصف هذا الموضوع الخطوات التي يجب اتباعها لتمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b0641-115">ويشرح أيضًا أنواع البيانات وتفاصيل التكوين التي يحتاج إليها التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b0641-116">تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="b0641-116">Enable the integration</span></span>

<span data-ttu-id="b0641-117">في Talent، يجب تشغيل التكامل وإدخال معلومات التكوين للاتصال بخدمة Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b0641-118">إذا أردت أن يتم استيراد حركة دفتر الأستاذ العام التي نشأت إلى Microsoft Dynamics 365 for Finance and Operations، فيجب أيضًا إعداد حساب في Microsoft Azure storage وإدخال سلسلة اتصال Azure Storage في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b0641-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="b0641-119">لتشغيل التكامل في Talent، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b0641-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="b0641-120">في صفحة **إدارة النظام**، حدد **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="b0641-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b0641-121">أدخل نقطة نهاية بروتوكول نقل الملفات (FTP) الآمنة ومسار مجلد FTP الآمن.</span><span class="sxs-lookup"><span data-stu-id="b0641-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b0641-122">أدخل اسم المستخدم وكلمة المرور للمستخدم الذي سينتقل إلى نقطة النهاية الآمنة ومسار المجلد الآمن في بروتوكول FTP.</span><span class="sxs-lookup"><span data-stu-id="b0641-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b0641-123">اختبر الاتصال، كما تقتضي الحاجة، وعيّن الخيار **تمكين تكامل كشف المرتبات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b0641-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b0641-124">عند تشغيل التكامل، يتم إنشاء حزمة وملفات تصدير البيانات ويتم تعيين معدل التكرار.</span><span class="sxs-lookup"><span data-stu-id="b0641-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b0641-125">ويمكنك تغيير معدل التكرار وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="b0641-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="b0641-126">لمزيد من المعلومات حول حسابات مساحة تخزين Azure وسلاسل اتصال مساحة تخزين Azure، راجع موضوعات Azure التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="b0641-127">حول حسابات مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="b0641-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b0641-128">تكوين سلاسل اتصال مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="b0641-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="b0641-129">تكوين بياناتك</span><span class="sxs-lookup"><span data-stu-id="b0641-129">Configure your data</span></span> 

<span data-ttu-id="b0641-130">لمعالجة كشف، يجب عليك تكوين بيانات الموارد البشرية في Talent.</span><span class="sxs-lookup"><span data-stu-id="b0641-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="b0641-131">يجب إعداد بيانات المؤسسة، مثل الوظائف والمناصب، مع معلومات الميزات والتعويضات.</span><span class="sxs-lookup"><span data-stu-id="b0641-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b0641-132">تتعلق هذه المعلومات بالتوظيف والدفع والخصم وهي معلومات مطلوبة لإنشاء عملية الدفع للموظفين.</span><span class="sxs-lookup"><span data-stu-id="b0641-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b0641-133">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="b0641-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b0641-134">ميزات</span><span class="sxs-lookup"><span data-stu-id="b0641-134">Benefits</span></span> 

<span data-ttu-id="b0641-135">توفر الموارد البشرية أدوات يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العاملين التي تقدمها مؤسسة أو تعالجها للعاملين فيها.</span><span class="sxs-lookup"><span data-stu-id="b0641-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b0641-136">عندما إنشاء ميزات، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b0641-137">خطط الميزات</span><span class="sxs-lookup"><span data-stu-id="b0641-137">Benefit plans</span></span>

- <span data-ttu-id="b0641-138">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-138">Plan (required)</span></span>
- <span data-ttu-id="b0641-139">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-139">Type (required)</span></span>
- <span data-ttu-id="b0641-140">تأثير كشف المرتبات (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-140">Payroll impact (required)</span></span>
- <span data-ttu-id="b0641-141">استرداد المتأخرات</span><span class="sxs-lookup"><span data-stu-id="b0641-141">Recover arrears</span></span>
- <span data-ttu-id="b0641-142">أسلوب الخصم</span><span class="sxs-lookup"><span data-stu-id="b0641-142">Deduction method</span></span>
- <span data-ttu-id="b0641-143">أولوية الخصم</span><span class="sxs-lookup"><span data-stu-id="b0641-143">Deduction priority</span></span>
- <span data-ttu-id="b0641-144">حد الفترة</span><span class="sxs-lookup"><span data-stu-id="b0641-144">Limit period</span></span>
- <span data-ttu-id="b0641-145">تحديد المبلغ</span><span class="sxs-lookup"><span data-stu-id="b0641-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b0641-146">ميزات</span><span class="sxs-lookup"><span data-stu-id="b0641-146">Benefits</span></span>

- <span data-ttu-id="b0641-147">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-147">Plan (required)</span></span>
- <span data-ttu-id="b0641-148">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-148">Type (required)</span></span>
- <span data-ttu-id="b0641-149">الخيار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-149">Option (required)</span></span>
- <span data-ttu-id="b0641-150">معرّف الميزة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-150">Benefit ID (required)</span></span>
- <span data-ttu-id="b0641-151">التكرار</span><span class="sxs-lookup"><span data-stu-id="b0641-151">Frequency</span></span>
- <span data-ttu-id="b0641-152">أساس</span><span class="sxs-lookup"><span data-stu-id="b0641-152">Basis</span></span>
- <span data-ttu-id="b0641-153">المبلغ أو النسبة</span><span class="sxs-lookup"><span data-stu-id="b0641-153">Amount or rate</span></span>
- <span data-ttu-id="b0641-154">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b0641-155">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b0641-155">Supported frequencies</span></span> 

- <span data-ttu-id="b0641-156">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="b0641-156">Weekly</span></span>
- <span data-ttu-id="b0641-157">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="b0641-157">Bi-weekly</span></span>
- <span data-ttu-id="b0641-158">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="b0641-158">Semi-monthly</span></span>
- <span data-ttu-id="b0641-159">شهري</span><span class="sxs-lookup"><span data-stu-id="b0641-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b0641-160">الأسس المدعومة</span><span class="sxs-lookup"><span data-stu-id="b0641-160">Supported bases</span></span> 

- <span data-ttu-id="b0641-161">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="b0641-161">Fixed amount</span></span>
- <span data-ttu-id="b0641-162">النسبة المئوية للأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-162">Percent of earnings</span></span>
- <span data-ttu-id="b0641-163">ساعات الإنتاج</span><span class="sxs-lookup"><span data-stu-id="b0641-163">Productive hours</span></span>

<span data-ttu-id="b0641-164">تنشئ خدمة Dayforce الخصومات التالية، استنادًا إلى تأثير كشف المرتبات المحدد في خطة الميزات.</span><span class="sxs-lookup"><span data-stu-id="b0641-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b0641-165">الاختيار في Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-165">Selection in Talent</span></span>        | <span data-ttu-id="b0641-166">النتيجة في Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b0641-167">بلا</span><span class="sxs-lookup"><span data-stu-id="b0641-167">None</span></span>                       | <span data-ttu-id="b0641-168">لا يتم إنشاء أي خصم.</span><span class="sxs-lookup"><span data-stu-id="b0641-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="b0641-169">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="b0641-169">Deduction only</span></span>             | <span data-ttu-id="b0641-170">يتم إنشاء خصم الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b0641-171">المساهمة فقط</span><span class="sxs-lookup"><span data-stu-id="b0641-171">Contribution only</span></span>          | <span data-ttu-id="b0641-172">يتم إنشاء خصم صاحب العمل‬.</span><span class="sxs-lookup"><span data-stu-id="b0641-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b0641-173">الخصم والمساهمة</span><span class="sxs-lookup"><span data-stu-id="b0641-173">Deduction and contribution</span></span> | <span data-ttu-id="b0641-174">يتم إنشاء خصومات الموظف وصاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="b0641-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b0641-175">لمزيد من المعلومات حول كيفية تحديد وإدارة برنامج ميزات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="b0641-176">تقديم برنامج ميزات الموظفين</span><span class="sxs-lookup"><span data-stu-id="b0641-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b0641-177">إنشاء ميزة جديدة</span><span class="sxs-lookup"><span data-stu-id="b0641-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b0641-178">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="b0641-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b0641-179">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="b0641-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b0641-180">التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-180">Compensation</span></span> 

<span data-ttu-id="b0641-181">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="b0641-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b0641-182">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="b0641-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b0641-183">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="b0641-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b0641-184">تستخدم خدمة Dayforce معلومات التعويض لحساب معدل الموظف السنوي أو الساعي.</span><span class="sxs-lookup"><span data-stu-id="b0641-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b0641-185">وتعتبر خطط التعويض الثابت وتحويلات معدل الدفع مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b0641-186">يجب ربط الموظفين بخطة تعويض ثابت.</span><span class="sxs-lookup"><span data-stu-id="b0641-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b0641-187">لمزيد من المعلومات حول خطط التعويض، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="b0641-188">إنشاء خطط التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="b0641-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b0641-189">إنشاء خطط التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="b0641-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b0641-190">تطوير خطط وبنية المرتب/التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b0641-191">تعويض العملية</span><span class="sxs-lookup"><span data-stu-id="b0641-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b0641-192">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="b0641-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b0641-193">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="b0641-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b0641-194">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="b0641-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b0641-195">الوظائف</span><span class="sxs-lookup"><span data-stu-id="b0641-195">Jobs</span></span> 

<span data-ttu-id="b0641-196">الوظيفة هي مجموعة من المهام والمسؤوليات المطلوبة من الشخص الذي يؤدي وظيفة.</span><span class="sxs-lookup"><span data-stu-id="b0641-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b0641-197">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b0641-198">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="b0641-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b0641-199">تحديد الوظائف الجديدة</span><span class="sxs-lookup"><span data-stu-id="b0641-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b0641-200">المناصب</span><span class="sxs-lookup"><span data-stu-id="b0641-200">Positions</span></span>

<span data-ttu-id="b0641-201">يعتبر المنصب مثيلاً فرديًا لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="b0641-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="b0641-202">على سبيل المثال، المنصب "مدير المبيعات (شرق)،" هو أحد المناصب المقترنة بالوظيفة، "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="b0641-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b0641-203">يوجد منصب في قسم.</span><span class="sxs-lookup"><span data-stu-id="b0641-203">A position exists in a department.</span></span> <span data-ttu-id="b0641-204">ويمكن ربط عامل واحد فقط بكل منصب.</span><span class="sxs-lookup"><span data-stu-id="b0641-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b0641-205">عند إعداد المناصب، يجب أخذ البيانات والتكوينات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="b0641-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b0641-206">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-206">Position (required)</span></span>
- <span data-ttu-id="b0641-207">الوصف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-207">Description (required)</span></span>
- <span data-ttu-id="b0641-208">الوظيف (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-208">Job (required)</span></span>
- <span data-ttu-id="b0641-209">القسم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-209">Department (required)</span></span>
- <span data-ttu-id="b0641-210">نوع المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-210">Position type (required)</span></span>
- <span data-ttu-id="b0641-211">مكافئ الوقت الكامل</span><span class="sxs-lookup"><span data-stu-id="b0641-211">Full-time equivalent</span></span>
- <span data-ttu-id="b0641-212">الساعات العادية السنوية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="b0641-213">الدفع بواسطة الكيان القانوني (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b0641-214">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-214">Pay cycle (required)</span></span>
- <span data-ttu-id="b0641-215">البعد المالي الافتراضي – مركز التكلفة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b0641-216">تعيين العامل – العامل وبدء التعيين وانتهاء التعيين وكود السبب</span><span class="sxs-lookup"><span data-stu-id="b0641-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b0641-217">عند ارتباط مناصب متعددة في القسم نفسه بالوظيفة نفسها، فسيتم دمجها في منصب واحد في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b0641-218">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b0641-219">تنظيم قوة العمل باستخدام الإدارات والوظائف والمناصب</span><span class="sxs-lookup"><span data-stu-id="b0641-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b0641-220">إعداد المناصب</span><span class="sxs-lookup"><span data-stu-id="b0641-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b0641-221">الأقسام</span><span class="sxs-lookup"><span data-stu-id="b0641-221">Departments</span></span>

<span data-ttu-id="b0641-222">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="b0641-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b0641-223">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="b0641-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b0641-224">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="b0641-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b0641-225">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="b0641-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b0641-226">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b0641-227">إنشاء قسم وإقرانه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="b0641-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b0641-228">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="b0641-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b0641-229">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="b0641-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="b0641-230">تحدد دورة الدفع معدل تكرار دفع المرتبات والأيام المحددة التي تُدفع فيها الأجور للعاملين.</span><span class="sxs-lookup"><span data-stu-id="b0641-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b0641-231">على سبيل المثال، قد تكون دورة الدفع الشهرية وقد تُدفع الأجور للعاملين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="b0641-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b0641-232">أو، قد تكون دورة الدفع أسبوعية وقد يحصل الموظفون على رواتبهم يوم الثلاثاء بعد انتهاء فترة الدفع.</span><span class="sxs-lookup"><span data-stu-id="b0641-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b0641-233">يتم تعيين دورات الدفع إلى مناصب للتحكم في الوقت الذي يتم فيه دفع أجور العاملين في هذه المناصب.</span><span class="sxs-lookup"><span data-stu-id="b0641-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b0641-234">بعد إنشاء دورات الدفع، يمكنك إنشاء فترات دفع لكل دورة.</span><span class="sxs-lookup"><span data-stu-id="b0641-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b0641-235">تتضمن كل فترة دفع تاريخ دفع افتراضيًا يستند إلى المعلومات التي توفرها.</span><span class="sxs-lookup"><span data-stu-id="b0641-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b0641-236">ومع ذلك، يمكنك تعديل تاريخ الدفع الافتراضي في فترة دفع للسماح بالاستثناءات، مثل عندما يقع تاريخ الدفع يوم عطلة.</span><span class="sxs-lookup"><span data-stu-id="b0641-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b0641-237">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b0641-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b0641-238">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-238">Pay cycle (required)</span></span>
- <span data-ttu-id="b0641-239">تكرار دورة الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b0641-240">تاريخ بدء الفترة (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b0641-241">تاريخ الدفع الافتراضي (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b0641-242">يتم دمج هذه المعلومات مع Dayforce كمجموعات دفع، ويتم فصلها حسب البلد أو المنطقة لكل دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="b0641-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b0641-243">يجب إنشاء فترة دفع واحدة على الأقل قبل الدمج.</span><span class="sxs-lookup"><span data-stu-id="b0641-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b0641-244">تقوم Dayforce بإنشاء تقويمات وتواريخ دفع للمجموعة، استنادًا إلى تاريخ بدء فترة الدفع الأولى وتاريخ الدفع الافتراضي الذي تم تحديده في Talent.</span><span class="sxs-lookup"><span data-stu-id="b0641-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b0641-245">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-245">Earning codes</span></span>

<span data-ttu-id="b0641-246">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b0641-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b0641-247">تحتوي أكواد الأرباح على معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b0641-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b0641-248">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="b0641-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b0641-249">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-249">Earning Code (required)</span></span>
- <span data-ttu-id="b0641-250">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-250">Description</span></span>
- <span data-ttu-id="b0641-251">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="b0641-251">Unit of measure</span></span>
- <span data-ttu-id="b0641-252">منتِج</span><span class="sxs-lookup"><span data-stu-id="b0641-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b0641-253">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-253">Worker data</span></span>

<span data-ttu-id="b0641-254">تعتبر السجلات الخاصة بمختلف أنواع العاملين مهمة لأنظمة الموارد البشرية وكشوف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="b0641-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b0641-255">يمكن استخدام المعلومات التي تقوم بإدخالها لتعقب العاملين والمعلومات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="b0641-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b0641-256">يمكنك المحافظة على المعلومات التالية للعاملين:</span><span class="sxs-lookup"><span data-stu-id="b0641-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b0641-257">**أساسية** – يمكنك المحافظة على معلومات أساسية حول عامل، مثل معلومات الاتصال والمعلومات الديموغرافية ومعلومات التعريف ومعلومات حول العائلة وحالة الخدمة العسكرية ومعلومات حول المغتربين وجهات الاتصال الشخصية وجهات الاتصال عند الطوارئ.</span><span class="sxs-lookup"><span data-stu-id="b0641-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b0641-258">**التوظيف** – يمكنك المحافظة على معلومات حول توظيف العامل، مثل معلومات حول شركة أو التبعية لمؤسسة وتعيين المنصب وتاريخي البدء والانتهاء والأهلية للعمل وشروط التوظيف والمعاش والإجازة، وتغيير الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="b0641-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b0641-259">**الإجازة والغياب** – يمكنك المحافظة على معلومات حول حالات غياب العامل، مثل تقويمات العمل وحركات الغياب وإعداد الغياب.</span><span class="sxs-lookup"><span data-stu-id="b0641-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b0641-260">**التعويض وكشف المرتبات** – يمكنك المحافظة على معلومات حول خطط تعويض العامل ومعلومات كشف المرتبات، مثل التسجيل في خطة والمكافآت والأداء والعمولة ومعلومات الضريبة والتقاعد والخصومات من الراتب.</span><span class="sxs-lookup"><span data-stu-id="b0641-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b0641-261">عند إدخال معلومات العامل، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b0641-262">معلومات عامة</span><span class="sxs-lookup"><span data-stu-id="b0641-262">General information</span></span>

- <span data-ttu-id="b0641-263">رقم الموظف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-263">Personnel number (required)</span></span>
- <span data-ttu-id="b0641-264">الاسم الأول (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-264">First name (required)</span></span>
- <span data-ttu-id="b0641-265">اسم العائلة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-265">Last name (required)</span></span>
- <span data-ttu-id="b0641-266">الاسم الأوسط</span><span class="sxs-lookup"><span data-stu-id="b0641-266">Middle name</span></span>
- <span data-ttu-id="b0641-267">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="b0641-267">Seniority date</span></span>
- <span data-ttu-id="b0641-268">معروف باسم</span><span class="sxs-lookup"><span data-stu-id="b0641-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b0641-269">معلومات شخصية</span><span class="sxs-lookup"><span data-stu-id="b0641-269">Personal information</span></span>

- <span data-ttu-id="b0641-270">الحالة الاجتماعية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-270">Marital status (required)</span></span>
- <span data-ttu-id="b0641-271">تاريخ الميلاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-271">Birth date (required)</span></span>
- <span data-ttu-id="b0641-272">الجنس (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-272">Gender (required)</span></span>
- <span data-ttu-id="b0641-273">شخص معاق</span><span class="sxs-lookup"><span data-stu-id="b0641-273">Person with disabilities</span></span>
- <span data-ttu-id="b0641-274">منطقة/بلد الجنسية (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b0641-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b0641-275">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="b0641-275">Address information</span></span>

- <span data-ttu-id="b0641-276">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-276">Primary (required)</span></span>
- <span data-ttu-id="b0641-277">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-277">Country/region (required)</span></span>
- <span data-ttu-id="b0641-278">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-278">Postal code (required)</span></span>
- <span data-ttu-id="b0641-279">رقم الشارع (مطلوب) (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b0641-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b0641-280">ملحق المبنى (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="b0641-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b0641-281">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-281">City (required)</span></span>
- <span data-ttu-id="b0641-282">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-282">State (required)</span></span>
- <span data-ttu-id="b0641-283">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b0641-284">معلومات الاتصال</span><span class="sxs-lookup"><span data-stu-id="b0641-284">Contact information</span></span> 

- <span data-ttu-id="b0641-285">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-285">Primary (required)</span></span>
- <span data-ttu-id="b0641-286">رقم الاتصال (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-286">Contact number (required)</span></span>
- <span data-ttu-id="b0641-287">الرقم الداخلي</span><span class="sxs-lookup"><span data-stu-id="b0641-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b0641-288">معلومات كشف المرتبات وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-288">Payroll information and earning codes</span></span>

<span data-ttu-id="b0641-289">قد يتم تعيين أرباح معينة للموظفين عند معدل تكرار دفع معين، وقد تكون لديهم طريقة دفع مفضلة.</span><span class="sxs-lookup"><span data-stu-id="b0641-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b0641-290">يتم استخدام الحقول التالية في Dayforce للمساعدة في ضمان استخدام هذه التفضيلات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="b0641-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b0641-291">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-291">Earning codes</span></span>

- <span data-ttu-id="b0641-292">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-292">Position (required)</span></span>
- <span data-ttu-id="b0641-293">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-293">Earning Code (required)</span></span>
- <span data-ttu-id="b0641-294">التكرار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-294">Frequency (required)</span></span>
- <span data-ttu-id="b0641-295">المبلغ (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b0641-296">معلومات الراتب</span><span class="sxs-lookup"><span data-stu-id="b0641-296">Payroll information</span></span>

- <span data-ttu-id="b0641-297">طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="b0641-297">Payment Method</span></span>
- <span data-ttu-id="b0641-298">المنطقة الاقتصادية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-298">Economic Region (required)</span></span>
- <span data-ttu-id="b0641-299">معرف ميزات الموظف</span><span class="sxs-lookup"><span data-stu-id="b0641-299">Employee Benefits ID</span></span>
- <span data-ttu-id="b0641-300">رقم المعرف القومي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-300">National ID Number (required)</span></span>
- <span data-ttu-id="b0641-301">رقم الخدمة العسكرية</span><span class="sxs-lookup"><span data-stu-id="b0641-301">Military Service Number</span></span>
- <span data-ttu-id="b0641-302">معرف الوردية (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-302">Shift ID (required)</span></span>
- <span data-ttu-id="b0641-303">رقم الضريبة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-303">Tax Number (required)</span></span>
- <span data-ttu-id="b0641-304">معرّف الاتحاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-304">Union ID (required)</span></span>
- <span data-ttu-id="b0641-305">معرّف يوم العمل (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-305">Work Day ID (required)</span></span>
- <span data-ttu-id="b0641-306">رقم تصريح العمل</span><span class="sxs-lookup"><span data-stu-id="b0641-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b0641-307">بالنسبة إلى طريقة الدفع، تدعم المكسيك الدفع **نقدًا** وبواسطة **شيك** (الشيك الفعلي للمؤسسة) و**الدفع الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="b0641-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b0641-308">إذا لم يتم تحديد أي طريقة دفع، فسيتم استخدام **الشيك** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="b0641-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b0641-309">تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="b0641-309">Employment details</span></span>

<span data-ttu-id="b0641-310">يتم استخدام سجل تفاصيل التوظيف كمعلومات أساسية لاستخراج حالات تعيين موظف وإنهاء خدماته وإعادة تعيينه في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b0641-311">تدعم خدمة Dayforce سجل توظيف نشط واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="b0641-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b0641-312">تاريخ بدء التوظيف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-312">Employment start date (required)</span></span>
- <span data-ttu-id="b0641-313">تاريخ انتهاء التوظيف</span><span class="sxs-lookup"><span data-stu-id="b0641-313">Employment end date</span></span>
- <span data-ttu-id="b0641-314">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="b0641-314">Start date</span></span>
- <span data-ttu-id="b0641-315">تاريخ البدء المعدل</span><span class="sxs-lookup"><span data-stu-id="b0641-315">Adjusted start date</span></span>
- <span data-ttu-id="b0641-316">تاريخ إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="b0641-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b0641-317">سبب إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="b0641-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b0641-318">يتم استخراج التواريخ الأساسية للموظف باستخدام المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="b0641-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b0641-319">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-319">Talent</span></span>                | <span data-ttu-id="b0641-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0641-321">أقرب تاريخ توظيف</span><span class="sxs-lookup"><span data-stu-id="b0641-321">Most recent hire date</span></span> | <span data-ttu-id="b0641-322">تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="b0641-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b0641-323">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="b0641-323">Termination date</span></span>      | <span data-ttu-id="b0641-324">تاريخ انتهاء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="b0641-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b0641-325">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="b0641-325">Start date</span></span>            | <span data-ttu-id="b0641-326">تاريخ البدء المعدل أو تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي غير النشط</span><span class="sxs-lookup"><span data-stu-id="b0641-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b0641-327">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="b0641-327">Original hire date</span></span>    | <span data-ttu-id="b0641-328">تاريخ بدء التوظيف في سجل محفوظات التوظيف الأحدث</span><span class="sxs-lookup"><span data-stu-id="b0641-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b0641-329">التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-329">Compensation</span></span>

<span data-ttu-id="b0641-330">يجب إقران خطة تعويض ثابت بالمنصب الأساسي لكل موظف خلال فترة التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b0641-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b0641-331">تبدأ هذه الفترة الزمنية في التاريخ الذي تم تعيين الموظف فيه (أو تاريخ بدء التوظيف) وتستمر حتى إنهاء خدمة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b0641-332">تاريخ السريان (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-332">Effective Date (required)</span></span>
- <span data-ttu-id="b0641-333">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b0641-333">Expiration date</span></span>
- <span data-ttu-id="b0641-334">معدل الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-334">Pay Rate (required)</span></span>
- <span data-ttu-id="b0641-335">تحويلات ‏‫معدل الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b0641-336">المكافئ السنوي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="b0641-337">المكافئ الساعي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="b0641-338">إذا كان لدى موظف ساعي مناصب متعددة، فسيتم استيراد التعويض الثابت للمنصب الأساسي إلى Dayforce كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b0641-339">فيما يتعلق بالمناصب غير الأساسية، يُحفظ المعدل الساعي إلى المنصب المناظر في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b0641-340">إذا كان لدى موظف يتلقى راتبًا مناصب متعددة، فسيتم استخراج المعدل الساعي التراكمي والراتب السنوي عبر كافة المناصب النشطة، وسيتم استخدامها كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b0641-341">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="b0641-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b0641-342">معرّف الضمان الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="b0641-342">Social Security identifier</span></span> 

<span data-ttu-id="b0641-343">يجب أن يكون لدى كل موظف معرّفًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="b0641-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b0641-344">يجب أن يكون هذا المعرّف من نوع التعريف‬ **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b0641-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b0641-345">في Dayforce، يتم استخراجه تلقائيًا على أنه معرّف الضمان الاجتماعي للموظف المطلوب للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="b0641-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b0641-346">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-346">Primary (required)</span></span>
- <span data-ttu-id="b0641-347">نوع التعريف = "SSN"</span><span class="sxs-lookup"><span data-stu-id="b0641-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b0641-348">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="b0641-348">Issued Date</span></span>
- <span data-ttu-id="b0641-349">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b0641-349">Expiration Date</span></span>

<span data-ttu-id="b0641-350">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b0641-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b0641-351">ومع ذلك، فإن السجل الذي سيتم دمجه في Dayforce هو فقط الذي يحمل العلامة **أساسي**، بصرف النظر عما إذا كان الرقم نشطًا أو منتهي الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="b0641-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b0641-352">الحسابات البنكية والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="b0641-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="b0641-353">يجب إدخال معلومات صالحة حول الحساب البنكي لأي موظف يختار تلقي الدفع من خلال تحويلات إلى الحساب البنكي‬.</span><span class="sxs-lookup"><span data-stu-id="b0641-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b0641-354">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-354">Talent</span></span>                         | <span data-ttu-id="b0641-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0641-356">رقم الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b0641-357">رمز SWIFT (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-357">SWIFT code (required)</span></span>          | <span data-ttu-id="b0641-358">حقل **معرّف البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b0641-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b0641-359">رقم الفرع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b0641-360">نوع الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-360">Bank account type (required)</span></span>   | <span data-ttu-id="b0641-361">حقل **نوع البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b0641-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b0641-362">تتضمن القيم المدعومة **شيكات** و**كشف المرتبات**.</span><span class="sxs-lookup"><span data-stu-id="b0641-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b0641-363">يتعين على الموظفين الذين اختاروا تلقي الدفع عبر تحويلات إلى الحساب البنكي‬ توفير ارتباط إلى حساب متبقٍ موجود ضمن كيان قانوني عنوانه الأساسي في المكسيك ويقترن بحساب بنكي صالح من بنك مكسيكي.</span><span class="sxs-lookup"><span data-stu-id="b0641-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b0641-364">يتم تجاهل كافة الحسابات الأخرى غير الحسابات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b0641-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b0641-365">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="b0641-365">Address information</span></span>

<span data-ttu-id="b0641-366">يجب أن يكون لدى كل موظف موقعًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="b0641-366">Every employee must have one primary location.</span></span> <span data-ttu-id="b0641-367">في Dayforce، يتم استخدام هذا الموقع لتحديد مكان الإقامة الأساسي للموظف لأغراض ضريبية.</span><span class="sxs-lookup"><span data-stu-id="b0641-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b0641-368">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-368">Primary (required)</span></span>
- <span data-ttu-id="b0641-369">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-369">Country/region (required)</span></span>
- <span data-ttu-id="b0641-370">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="b0641-371">الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-371">Street (required)</span></span>
- <span data-ttu-id="b0641-372">رقم الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-372">Street Number (required)</span></span>
- <span data-ttu-id="b0641-373">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="b0641-373">Building Complement</span></span>
- <span data-ttu-id="b0641-374">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-374">City (required)</span></span>
- <span data-ttu-id="b0641-375">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-375">State (required)</span></span>
- <span data-ttu-id="b0641-376">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b0641-377">تكوين البيانات لإنشاء كشف مرتبات في الولايات المتحدة وكندا</span><span class="sxs-lookup"><span data-stu-id="b0641-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b0641-378">إذا كنت تقوم بإنشاء الدفع للموظفين في الولايات المتحدة وكندا، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b0641-379">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="b0641-379">Departments are required on positions.</span></span>
- <span data-ttu-id="b0641-380">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b0641-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="b0641-381">يمكنك تكوين Talent لمطالبة المناصب بتحديد قسم.</span><span class="sxs-lookup"><span data-stu-id="b0641-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="b0641-382">للقيام بذلك، انتقل إلى **الموارد البشرية المناصب المشتركة > المناصب > الأقسام مطلوبة على المناصب**.</span><span class="sxs-lookup"><span data-stu-id="b0641-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="b0641-383">من المستحسن أن يتم فرض هذا الإعداد للتكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="b0641-384">أنواع الوظائف</span><span class="sxs-lookup"><span data-stu-id="b0641-384">Job types</span></span>

<span data-ttu-id="b0641-385">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="b0641-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b0641-386">تعتبر أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في الولايات المتحدة وكندا.</span><span class="sxs-lookup"><span data-stu-id="b0641-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b0641-387">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="b0641-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b0641-388">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="b0641-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b0641-389">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b0641-390">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b0641-390">Job type</span></span>   | <span data-ttu-id="b0641-391">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b0641-392">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b0641-392">Hourly</span></span>     | <span data-ttu-id="b0641-393">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b0641-393">Hourly</span></span>      |
| <span data-ttu-id="b0641-394">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b0641-394">Salaried</span></span>   | <span data-ttu-id="b0641-395">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b0641-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b0641-396">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="b0641-396">Position types</span></span> 

<span data-ttu-id="b0641-397">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="b0641-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b0641-398">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="b0641-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b0641-399">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b0641-400">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="b0641-400">Position type</span></span>   | <span data-ttu-id="b0641-401">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b0641-402">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="b0641-402">Full-time</span></span>       | <span data-ttu-id="b0641-403">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="b0641-403">Full time employee</span></span> |
| <span data-ttu-id="b0641-404">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b0641-404">Part-time</span></span>       | <span data-ttu-id="b0641-405">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b0641-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b0641-406">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="b0641-406">Reason codes</span></span>

<span data-ttu-id="b0641-407">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b0641-408">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="b0641-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b0641-409">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b0641-410">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="b0641-410">Reason code</span></span>    | <span data-ttu-id="b0641-411">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-411">Description</span></span>      | <span data-ttu-id="b0641-412">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b0641-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b0641-413">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b0641-413">RESIGNATION</span></span>    | <span data-ttu-id="b0641-414">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b0641-414">Resignation</span></span>      | <span data-ttu-id="b0641-415">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-415">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-416">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0641-416">TERMINATION</span></span>    | <span data-ttu-id="b0641-417">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0641-417">Termination</span></span>      | <span data-ttu-id="b0641-418">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-418">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-419">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b0641-419">RETIREMENT</span></span>     | <span data-ttu-id="b0641-420">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b0641-420">Retirement</span></span>       | <span data-ttu-id="b0641-421">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-421">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-422">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b0641-422">OTHER</span></span>          | <span data-ttu-id="b0641-423">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="b0641-423">Other Reasons</span></span>    | <span data-ttu-id="b0641-424">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-424">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-425">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b0641-425">DEATH</span></span>          | <span data-ttu-id="b0641-426">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b0641-426">Death</span></span>            | <span data-ttu-id="b0641-427">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-427">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b0641-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b0641-429">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="b0641-429">Leave of Absence</span></span> | <span data-ttu-id="b0641-430">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-430">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b0641-431">CONTRACTEND</span></span>    | <span data-ttu-id="b0641-432">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="b0641-432">End of Contract</span></span>  | <span data-ttu-id="b0641-433">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-433">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b0641-434">SALARYCHANGE</span></span>   | <span data-ttu-id="b0641-435">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="b0641-435">Change of Salary</span></span> | <span data-ttu-id="b0641-436">التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b0641-437">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="b0641-437">Marital status</span></span>

<span data-ttu-id="b0641-438">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b0641-439">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b0641-440">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-440">Talent</span></span>                 | <span data-ttu-id="b0641-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b0641-442">متزوج</span><span class="sxs-lookup"><span data-stu-id="b0641-442">Married</span></span>                | <span data-ttu-id="b0641-443">متزوج</span><span class="sxs-lookup"><span data-stu-id="b0641-443">Married</span></span>              |
| <span data-ttu-id="b0641-444">واحد</span><span class="sxs-lookup"><span data-stu-id="b0641-444">Single</span></span>                 | <span data-ttu-id="b0641-445">واحد</span><span class="sxs-lookup"><span data-stu-id="b0641-445">Single</span></span>               |
| <span data-ttu-id="b0641-446">أرمل</span><span class="sxs-lookup"><span data-stu-id="b0641-446">Widowed</span></span>                | <span data-ttu-id="b0641-447">أرمل</span><span class="sxs-lookup"><span data-stu-id="b0641-447">Widowed</span></span>              |
| <span data-ttu-id="b0641-448">مطلق</span><span class="sxs-lookup"><span data-stu-id="b0641-448">Divorced</span></span>               | <span data-ttu-id="b0641-449">مطلق</span><span class="sxs-lookup"><span data-stu-id="b0641-449">Divorced</span></span>             |
| <span data-ttu-id="b0641-450">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="b0641-450">Registered Partnership</span></span> | <span data-ttu-id="b0641-451">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="b0641-451">Domestic Partnership</span></span> |
| <span data-ttu-id="b0641-452">بلا</span><span class="sxs-lookup"><span data-stu-id="b0641-452">None</span></span>                   | <span data-ttu-id="b0641-453">بلا</span><span class="sxs-lookup"><span data-stu-id="b0641-453">None</span></span>                 |
| <span data-ttu-id="b0641-454">تعايش</span><span class="sxs-lookup"><span data-stu-id="b0641-454">Cohabiting</span></span>             | <span data-ttu-id="b0641-455">تعايش</span><span class="sxs-lookup"><span data-stu-id="b0641-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b0641-456">الجنس</span><span class="sxs-lookup"><span data-stu-id="b0641-456">Gender</span></span>

<span data-ttu-id="b0641-457">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b0641-458">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b0641-459">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-459">Talent</span></span>       | <span data-ttu-id="b0641-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b0641-461">ذكر</span><span class="sxs-lookup"><span data-stu-id="b0641-461">Male</span></span>         | <span data-ttu-id="b0641-462">ذكر</span><span class="sxs-lookup"><span data-stu-id="b0641-462">Male</span></span>            |
| <span data-ttu-id="b0641-463">أنثى</span><span class="sxs-lookup"><span data-stu-id="b0641-463">Female</span></span>       | <span data-ttu-id="b0641-464">أنثى</span><span class="sxs-lookup"><span data-stu-id="b0641-464">Female</span></span>          |
| <span data-ttu-id="b0641-465">غير محدد</span><span class="sxs-lookup"><span data-stu-id="b0641-465">Non-specific</span></span> | <span data-ttu-id="b0641-466">*غير مدعوم*</span><span class="sxs-lookup"><span data-stu-id="b0641-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b0641-467">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-467">Earning codes</span></span>

<span data-ttu-id="b0641-468">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b0641-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b0641-469">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b0641-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b0641-470">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="b0641-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b0641-471">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b0641-471">Supported frequencies</span></span>

- <span data-ttu-id="b0641-472">الكل</span><span class="sxs-lookup"><span data-stu-id="b0641-472">All</span></span>
- <span data-ttu-id="b0641-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b0641-473">EVERYPAY</span></span>
- <span data-ttu-id="b0641-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b0641-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b0641-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b0641-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b0641-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b0641-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b0641-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-477">1OFMTH</span></span>
- <span data-ttu-id="b0641-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-478">LASTOFMTH</span></span>
- <span data-ttu-id="b0641-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-479">2OFMTH</span></span>
- <span data-ttu-id="b0641-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-480">3OFMTH</span></span>
- <span data-ttu-id="b0641-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-481">4OFMTH</span></span>
- <span data-ttu-id="b0641-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-482">5OFMTH</span></span>
- <span data-ttu-id="b0641-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-483">1N2OFMTH</span></span>
- <span data-ttu-id="b0641-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-484">3N4OFMTH</span></span>
- <span data-ttu-id="b0641-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-485">1N3OFMTH</span></span>
- <span data-ttu-id="b0641-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-486">1N4OFMTH</span></span>
- <span data-ttu-id="b0641-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-487">2N3OFMTH</span></span>
- <span data-ttu-id="b0641-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-488">2N4OFMTH</span></span>
- <span data-ttu-id="b0641-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="b0641-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="b0641-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b0641-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b0641-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b0641-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b0641-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b0641-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b0641-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b0641-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b0641-501">العناوين</span><span class="sxs-lookup"><span data-stu-id="b0641-501">Addresses</span></span>

<span data-ttu-id="b0641-502">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="b0641-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b0641-503">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="b0641-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b0641-504">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-504">Talent</span></span>          | <span data-ttu-id="b0641-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b0641-506">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="b0641-506">Country/Region</span></span>  | <span data-ttu-id="b0641-507">كود البلد</span><span class="sxs-lookup"><span data-stu-id="b0641-507">Country Code</span></span>          |
| <span data-ttu-id="b0641-508">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b0641-508">Zip/Postal Code</span></span> | <span data-ttu-id="b0641-509">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b0641-509">Postal Code</span></span>           |
| <span data-ttu-id="b0641-510">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="b0641-510">State</span></span>           | <span data-ttu-id="b0641-511">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="b0641-511">State Code</span></span>            |
| <span data-ttu-id="b0641-512">المدينة</span><span class="sxs-lookup"><span data-stu-id="b0641-512">City</span></span>            | <span data-ttu-id="b0641-513">المدينة</span><span class="sxs-lookup"><span data-stu-id="b0641-513">City</span></span>                  |
| <span data-ttu-id="b0641-514">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b0641-514">County</span></span>          | <span data-ttu-id="b0641-515">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="b0641-515">County (Municipality)</span></span> |
| <span data-ttu-id="b0641-516">الشارع</span><span class="sxs-lookup"><span data-stu-id="b0641-516">Street</span></span>          | <span data-ttu-id="b0641-517">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="b0641-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b0641-518">مناطق الضريبة</span><span class="sxs-lookup"><span data-stu-id="b0641-518">Tax regions</span></span>

<span data-ttu-id="b0641-519">تُستخدم مناطق الضريبة لتحديد الضريبة المناسبة التي يجب تطبيقها أثناء إنشاء كشف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="b0641-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b0641-520">يتم تعيين مناطق الضريبة إلى Dayforce كعناوين موقع.</span><span class="sxs-lookup"><span data-stu-id="b0641-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b0641-521">يجب أن تكون منطقة الضريبة الافتراضية مقترنة بمنصب العامل النشط.</span><span class="sxs-lookup"><span data-stu-id="b0641-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b0641-522">منطقة الضريبة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-522">Tax region (required)</span></span>
- <span data-ttu-id="b0641-523">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="b0641-523">Country/Region (required)</span></span>
- <span data-ttu-id="b0641-524">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-524">State (required)</span></span>
- <span data-ttu-id="b0641-525">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b0641-525">County</span></span> 
- <span data-ttu-id="b0641-526">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="b0641-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b0641-527">تكوين بياناتك لإنشاء كشف المرتبات في المكسيك</span><span class="sxs-lookup"><span data-stu-id="b0641-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b0641-528">إذا كنت تقوم بإنشاء الدفع للموظفين في المكسيك، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="b0641-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b0641-529">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="b0641-529">Departments are required on positions.</span></span>
- <span data-ttu-id="b0641-530">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="b0641-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b0641-531">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b0641-531">Job types</span></span>

<span data-ttu-id="b0641-532">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="b0641-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b0641-533">أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="b0641-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b0641-534">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="b0641-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b0641-535">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="b0641-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b0641-536">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b0641-537">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="b0641-537">Job type</span></span>   | <span data-ttu-id="b0641-538">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b0641-539">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="b0641-539">Hourly</span></span>     | <span data-ttu-id="b0641-540">الحد الأقصى للأجر في الساعة‬</span><span class="sxs-lookup"><span data-stu-id="b0641-540">MX Hourly</span></span>   |
| <span data-ttu-id="b0641-541">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="b0641-541">Salaried</span></span>   | <span data-ttu-id="b0641-542">الحد الأقصى للراتب</span><span class="sxs-lookup"><span data-stu-id="b0641-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b0641-543">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="b0641-543">Position types</span></span> 

<span data-ttu-id="b0641-544">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="b0641-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b0641-545">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="b0641-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b0641-546">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b0641-547">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="b0641-547">Position type</span></span>   | <span data-ttu-id="b0641-548">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b0641-549">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="b0641-549">Full-time</span></span>       | <span data-ttu-id="b0641-550">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="b0641-550">Full time employee</span></span> |
| <span data-ttu-id="b0641-551">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b0641-551">Part-time</span></span>       | <span data-ttu-id="b0641-552">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="b0641-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b0641-553">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="b0641-553">Reason codes</span></span>

<span data-ttu-id="b0641-554">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="b0641-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b0641-555">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="b0641-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b0641-556">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b0641-557">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="b0641-557">Reason code</span></span>            | <span data-ttu-id="b0641-558">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-558">Description</span></span>                    | <span data-ttu-id="b0641-559">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b0641-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b0641-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b0641-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b0641-561">المغادرة قبل كشف المرتبات الأول</span><span class="sxs-lookup"><span data-stu-id="b0641-561">Departure before first payroll</span></span> | <span data-ttu-id="b0641-562">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-562">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-563">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b0641-563">RESIGNATION</span></span>            | <span data-ttu-id="b0641-564">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="b0641-564">Resignation</span></span>                    | <span data-ttu-id="b0641-565">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-565">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-566">المعاش</span><span class="sxs-lookup"><span data-stu-id="b0641-566">PENSION</span></span>                | <span data-ttu-id="b0641-567">المعاش</span><span class="sxs-lookup"><span data-stu-id="b0641-567">Pension</span></span>                        | <span data-ttu-id="b0641-568">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-568">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-569">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0641-569">TERMINATION</span></span>            | <span data-ttu-id="b0641-570">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="b0641-570">Termination</span></span>                    | <span data-ttu-id="b0641-571">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-571">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-572">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b0641-572">RETIREMENT</span></span>             | <span data-ttu-id="b0641-573">التقاعد</span><span class="sxs-lookup"><span data-stu-id="b0641-573">Retirement</span></span>                     | <span data-ttu-id="b0641-574">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-574">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-575">الغائب</span><span class="sxs-lookup"><span data-stu-id="b0641-575">ABSENTEE</span></span>               | <span data-ttu-id="b0641-576">الغائب</span><span class="sxs-lookup"><span data-stu-id="b0641-576">Absentee</span></span>                       | <span data-ttu-id="b0641-577">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-577">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-578">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b0641-578">OTHER</span></span>                  | <span data-ttu-id="b0641-579">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="b0641-579">Other Reasons</span></span>                  | <span data-ttu-id="b0641-580">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-580">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-581">إقفال</span><span class="sxs-lookup"><span data-stu-id="b0641-581">CLOSURE</span></span>                | <span data-ttu-id="b0641-582">إقفال الشركة</span><span class="sxs-lookup"><span data-stu-id="b0641-582">Business Closure</span></span>               | <span data-ttu-id="b0641-583">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-583">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-584">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b0641-584">DEATH</span></span>                  | <span data-ttu-id="b0641-585">الوفاة</span><span class="sxs-lookup"><span data-stu-id="b0641-585">Death</span></span>                          | <span data-ttu-id="b0641-586">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-586">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b0641-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b0641-588">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="b0641-588">Leave of Absence</span></span>               | <span data-ttu-id="b0641-589">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-589">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b0641-590">CONTRACTEND</span></span>            | <span data-ttu-id="b0641-591">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="b0641-591">End of Contract</span></span>                | <span data-ttu-id="b0641-592">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="b0641-592">Terminate worker</span></span>     |
| <span data-ttu-id="b0641-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b0641-593">SALARYCHANGE</span></span>           | <span data-ttu-id="b0641-594">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="b0641-594">Change of Salary</span></span>               | <span data-ttu-id="b0641-595">التعويض</span><span class="sxs-lookup"><span data-stu-id="b0641-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b0641-596">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="b0641-596">Terms of employment</span></span>

<span data-ttu-id="b0641-597">يتم استخدام شروط التوظيف لإنشاء فئات شروط التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b0641-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b0641-598">يتم تعيين الشروط إلى Dayforce كقيم مؤشر التوظيف.</span><span class="sxs-lookup"><span data-stu-id="b0641-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b0641-599">شروط التوظيف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b0641-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b0641-600">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="b0641-600">Terms of employment</span></span>   | <span data-ttu-id="b0641-601">الوصف</span><span class="sxs-lookup"><span data-stu-id="b0641-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b0641-602">عادي</span><span class="sxs-lookup"><span data-stu-id="b0641-602">Regular</span></span>               | <span data-ttu-id="b0641-603">عادي</span><span class="sxs-lookup"><span data-stu-id="b0641-603">Regular</span></span>     |
| <span data-ttu-id="b0641-604">مباشر</span><span class="sxs-lookup"><span data-stu-id="b0641-604">Direct</span></span>                | <span data-ttu-id="b0641-605">مباشر</span><span class="sxs-lookup"><span data-stu-id="b0641-605">Direct</span></span>      |
| <span data-ttu-id="b0641-606">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="b0641-606">Internship</span></span>            | <span data-ttu-id="b0641-607">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="b0641-607">Internship</span></span>  |
| <span data-ttu-id="b0641-608">دائم</span><span class="sxs-lookup"><span data-stu-id="b0641-608">Permanent</span></span>             | <span data-ttu-id="b0641-609">دائم</span><span class="sxs-lookup"><span data-stu-id="b0641-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b0641-610">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="b0641-610">Marital status</span></span>

<span data-ttu-id="b0641-611">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b0641-612">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b0641-613">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-613">Talent</span></span>                 | <span data-ttu-id="b0641-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b0641-615">متزوج</span><span class="sxs-lookup"><span data-stu-id="b0641-615">Married</span></span>                | <span data-ttu-id="b0641-616">متزوج</span><span class="sxs-lookup"><span data-stu-id="b0641-616">Married</span></span>                   |
| <span data-ttu-id="b0641-617">واحد</span><span class="sxs-lookup"><span data-stu-id="b0641-617">Single</span></span>                 | <span data-ttu-id="b0641-618">واحد</span><span class="sxs-lookup"><span data-stu-id="b0641-618">Single</span></span>                    |
| <span data-ttu-id="b0641-619">أرمل</span><span class="sxs-lookup"><span data-stu-id="b0641-619">Widowed</span></span>                | <span data-ttu-id="b0641-620">أرمل</span><span class="sxs-lookup"><span data-stu-id="b0641-620">Widowed</span></span>                   |
| <span data-ttu-id="b0641-621">مطلق</span><span class="sxs-lookup"><span data-stu-id="b0641-621">Divorced</span></span>               | <span data-ttu-id="b0641-622">مطلق</span><span class="sxs-lookup"><span data-stu-id="b0641-622">Divorced</span></span>                  |
| <span data-ttu-id="b0641-623">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="b0641-623">Registered Partnership</span></span> | <span data-ttu-id="b0641-624">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="b0641-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="b0641-625">بلا</span><span class="sxs-lookup"><span data-stu-id="b0641-625">None</span></span>                   | <span data-ttu-id="b0641-626">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b0641-627">تعايش</span><span class="sxs-lookup"><span data-stu-id="b0641-627">Cohabiting</span></span>             | <span data-ttu-id="b0641-628">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b0641-629">الجنس</span><span class="sxs-lookup"><span data-stu-id="b0641-629">Gender</span></span>

<span data-ttu-id="b0641-630">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b0641-631">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b0641-632">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-632">Talent</span></span>       | <span data-ttu-id="b0641-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b0641-634">ذكر</span><span class="sxs-lookup"><span data-stu-id="b0641-634">Male</span></span>         | <span data-ttu-id="b0641-635">ذكر</span><span class="sxs-lookup"><span data-stu-id="b0641-635">Male</span></span>                      |
| <span data-ttu-id="b0641-636">أنثى</span><span class="sxs-lookup"><span data-stu-id="b0641-636">Female</span></span>       | <span data-ttu-id="b0641-637">أنثى</span><span class="sxs-lookup"><span data-stu-id="b0641-637">Female</span></span>                    |
| <span data-ttu-id="b0641-638">غير محدد</span><span class="sxs-lookup"><span data-stu-id="b0641-638">Non-specific</span></span> | <span data-ttu-id="b0641-639">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b0641-640">أسلوب الدفع</span><span class="sxs-lookup"><span data-stu-id="b0641-640">Payment method</span></span>

<span data-ttu-id="b0641-641">تقدم طرق دفع للموظف والشركة طريقة لوصف كيفية تسديد مرتبات وأجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="b0641-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b0641-642">يتم تعيين طرق الدفع إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b0641-643">يعرض الجدول التالي كيفية تعيين طرق الدفع إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b0641-644">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-644">Talent</span></span>             | <span data-ttu-id="b0641-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b0641-646">نقدي</span><span class="sxs-lookup"><span data-stu-id="b0641-646">Cash</span></span>               | <span data-ttu-id="b0641-647">نقدي</span><span class="sxs-lookup"><span data-stu-id="b0641-647">Cash</span></span>                      |
| <span data-ttu-id="b0641-648">دفع إلكتروني</span><span class="sxs-lookup"><span data-stu-id="b0641-648">Electronic Payment</span></span> | <span data-ttu-id="b0641-649">التحويل</span><span class="sxs-lookup"><span data-stu-id="b0641-649">Transfer</span></span>                  |
| <span data-ttu-id="b0641-650">فحص</span><span class="sxs-lookup"><span data-stu-id="b0641-650">Check</span></span>              | <span data-ttu-id="b0641-651">شيك</span><span class="sxs-lookup"><span data-stu-id="b0641-651">Cheque</span></span>                    |
| <span data-ttu-id="b0641-652">حوالة مصرفية</span><span class="sxs-lookup"><span data-stu-id="b0641-652">Bank Draft</span></span>         | <span data-ttu-id="b0641-653">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b0641-654">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="b0641-654">Other</span></span>              | <span data-ttu-id="b0641-655">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b0641-656">نوع الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="b0641-656">Bank account type</span></span>

<span data-ttu-id="b0641-657">يتم استخدام أنواع الحسابات البنكية للدفع الإلكتروني للموظفين.</span><span class="sxs-lookup"><span data-stu-id="b0641-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b0641-658">يتم تعيين أنواع الحسابات البنكية إلى Dayforce كمعلومات حساب التحويل.</span><span class="sxs-lookup"><span data-stu-id="b0641-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b0641-659">وتتم ترجمة أنواع الحسابات البنكية، كما هو مناسب، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="b0641-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b0641-660">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-660">Talent</span></span>            | <span data-ttu-id="b0641-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b0641-662">حساب شيكات</span><span class="sxs-lookup"><span data-stu-id="b0641-662">Checking Account</span></span>  | <span data-ttu-id="b0641-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="b0641-663">CheckingAccount</span></span>           |
| <span data-ttu-id="b0641-664">حساب الراتب</span><span class="sxs-lookup"><span data-stu-id="b0641-664">Payroll Account</span></span>   | <span data-ttu-id="b0641-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b0641-665">PayrollAccount</span></span>            |
| <span data-ttu-id="b0641-666">حساب توفير</span><span class="sxs-lookup"><span data-stu-id="b0641-666">Savings Account</span></span>   | <span data-ttu-id="b0641-667">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b0641-668">حساب BankGirot</span><span class="sxs-lookup"><span data-stu-id="b0641-668">BankGirot account</span></span> | <span data-ttu-id="b0641-669">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b0641-670">حساب PlusGirot</span><span class="sxs-lookup"><span data-stu-id="b0641-670">PlusGirot account</span></span> | <span data-ttu-id="b0641-671">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="b0641-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b0641-672">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="b0641-672">Earning codes</span></span>

<span data-ttu-id="b0641-673">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="b0641-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b0641-674">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b0641-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b0641-675">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="b0641-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b0641-676">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="b0641-676">Supported frequencies</span></span>

- <span data-ttu-id="b0641-677">الكل</span><span class="sxs-lookup"><span data-stu-id="b0641-677">All</span></span>
- <span data-ttu-id="b0641-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b0641-678">EVERYPAY</span></span>
- <span data-ttu-id="b0641-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b0641-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b0641-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b0641-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b0641-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b0641-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b0641-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-682">1OFMTH</span></span>
- <span data-ttu-id="b0641-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-683">LASTOFMTH</span></span>
- <span data-ttu-id="b0641-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-684">2OFMTH</span></span>
- <span data-ttu-id="b0641-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-685">3OFMTH</span></span>
- <span data-ttu-id="b0641-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-686">4OFMTH</span></span>
- <span data-ttu-id="b0641-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-687">5OFMTH</span></span>
- <span data-ttu-id="b0641-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-688">1N2OFMTH</span></span>
- <span data-ttu-id="b0641-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-689">3N4OFMTH</span></span>
- <span data-ttu-id="b0641-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-690">1N3OFMTH</span></span>
- <span data-ttu-id="b0641-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-691">1N4OFMTH</span></span>
- <span data-ttu-id="b0641-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-692">2N3OFMTH</span></span>
- <span data-ttu-id="b0641-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-693">2N4OFMTH</span></span>
- <span data-ttu-id="b0641-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="b0641-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="b0641-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b0641-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b0641-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b0641-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b0641-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b0641-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b0641-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b0641-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b0641-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b0641-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b0641-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b0641-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b0641-706">العناوين</span><span class="sxs-lookup"><span data-stu-id="b0641-706">Addresses</span></span>

<span data-ttu-id="b0641-707">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="b0641-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b0641-708">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="b0641-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b0641-709">Talent</span><span class="sxs-lookup"><span data-stu-id="b0641-709">Talent</span></span>              | <span data-ttu-id="b0641-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b0641-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b0641-711">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="b0641-711">Country/Region</span></span>      | <span data-ttu-id="b0641-712">كود البلد</span><span class="sxs-lookup"><span data-stu-id="b0641-712">Country Code</span></span>          |
| <span data-ttu-id="b0641-713">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b0641-713">Zip/Postal Code</span></span>     | <span data-ttu-id="b0641-714">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="b0641-714">Postal Code</span></span>           |
| <span data-ttu-id="b0641-715">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="b0641-715">State</span></span>               | <span data-ttu-id="b0641-716">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="b0641-716">State Code</span></span>            |
| <span data-ttu-id="b0641-717">المدينة</span><span class="sxs-lookup"><span data-stu-id="b0641-717">City</span></span>                | <span data-ttu-id="b0641-718">المدينة</span><span class="sxs-lookup"><span data-stu-id="b0641-718">City</span></span>                  |
| <span data-ttu-id="b0641-719">الإقليم</span><span class="sxs-lookup"><span data-stu-id="b0641-719">County</span></span>              | <span data-ttu-id="b0641-720">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="b0641-720">County (Municipality)</span></span> |
| <span data-ttu-id="b0641-721">الشارع</span><span class="sxs-lookup"><span data-stu-id="b0641-721">Street</span></span>              | <span data-ttu-id="b0641-722">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="b0641-722">Address Line 1</span></span>        |
| <span data-ttu-id="b0641-723">رقم الشارع</span><span class="sxs-lookup"><span data-stu-id="b0641-723">Street Number</span></span>       | <span data-ttu-id="b0641-724">سطر العنوان 2</span><span class="sxs-lookup"><span data-stu-id="b0641-724">Address Line 2</span></span>        |
| <span data-ttu-id="b0641-725">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="b0641-725">Building Complement</span></span> | <span data-ttu-id="b0641-726">سطر العنوان 5</span><span class="sxs-lookup"><span data-stu-id="b0641-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b0641-727">رقم جواز السفر</span><span class="sxs-lookup"><span data-stu-id="b0641-727">Passport number</span></span>

<span data-ttu-id="b0641-728">بإمكان الموظفين إعلان معلومات جواز السفر.</span><span class="sxs-lookup"><span data-stu-id="b0641-728">Employees can declare passport information.</span></span> <span data-ttu-id="b0641-729">هذه المعلومات هي نوع من أنواع تعريف **جواز السفر** وهي تتكامل في Dayforce كجزء من معلومات الموظف خاصة بالمكسيك.</span><span class="sxs-lookup"><span data-stu-id="b0641-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b0641-730">نوع التعريف = "جواز سفر"</span><span class="sxs-lookup"><span data-stu-id="b0641-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b0641-731">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="b0641-731">Issued Date</span></span>
- <span data-ttu-id="b0641-732">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="b0641-732">Expiration Date</span></span>

<span data-ttu-id="b0641-733">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **جواز سفر**.</span><span class="sxs-lookup"><span data-stu-id="b0641-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b0641-734">ومع ذلك، يتم دمج إدخال جواز السفر النشط الحالي فقط في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b0641-735">إذا انتهت صلاحية جميع إدخالات جوازات السفر، فسيتكامل جواز السفر الذي تم إصداره مؤخرًا في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b0641-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
